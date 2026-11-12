# TurnKey E Blend for iDrive 8

TurnKey E Blend estimates how much ethanol is in the tank after a refill and calculates how much petrol and E85 to add for a target blend. It uses litres and supports English and Ukrainian.

## Install or update in MGU Store

1. Open **Settings → Add source** in MGU Store and enter `vecyoroleg-lgtm/turnkey-e-blend-id8`.
2. Choose **Releases**. You can also add the [HTTPS catalogue](https://raw.githubusercontent.com/vecyoroleg-lgtm/turnkey-e-blend-id8/main/catalog.json) as a source.
3. Select **TurnKey E Blend → Install**. If the app is already installed, select **Update**. Restart iDrive if MGU Store prompts you.

## Calculate a blend

Open **TurnKey E Blend** from the iDrive app menu. Enter the tank capacity and the fuel remaining in the tank. Set **Fuel after refill** to the total volume you want in the tank, including the fuel already there. The default is **Full tank**. To restore it, open **Fuel after refill** and select **Use full tank**.

Select **Read fuel from car** to fill **Fuel in tank** with the instrument cluster's current fuel volume. If you see **Fuel unavailable · Retry**, tap again or edit **Fuel in tank** manually. The reading supplies volume in litres. Enter the ethanol percentages separately.

Enter the ethanol percentages of the fuel in the tank and both fuels at the pump, and set **Target ethanol**. For E100, enter 100% in **Ethanol in E85**. Select **Save** after each entry, then select **Calculate**. You can leave **Ethanol in tank** blank when the tank is empty.

The result shows the litres of petrol and E85 to add, the expected ethanol percentage, and the total fuel volume. If the target ethanol percentage is outside the range achievable at the selected volume, the app displays that range. Values stay available while the app is running.

## Language

Open **Language / Мова** on the main screen and choose **English** or **Українська**. The app remembers your choice.

## Estimate tank ethanol

Select **Estimate tank ethanol**. Enter the fuel volume and ethanol percentage from before the refill, then enter the litres and ethanol percentage of each fuel you added. Enter **0 L** for an empty tank before refilling and leave unused fuels at **0 L**. Select **Calculate** to see the estimated ethanol percentage, the litres of ethanol and the total fuel volume. Each fuel portion above **0 L** needs an ethanol percentage.

## Source code and USB build

Download the source archive from the [release page](https://github.com/vecyoroleg-lgtm/turnkey-e-blend-id8/releases/tag/catalog). To build the USB package, extract the archive alongside the [pinned MGU Store source](https://github.com/robertnisipeanu/mgu-store/tree/7dffddd8c3d9efe171f790beb37aba36c41e062e) in a directory named `mgu-store` and run `python build.py` from the app directory with Python 3.9+ and Node.js 18+ available. The build writes the versioned USB archive to `dist`.

Extract the USB archive so `mgu-repo` sits at the root of the drive. Plug it into a data USB port and open **USB** in MGU Store to install. MGU Store builds the native app using the head unit's SDK.

This app is a beta. Testing on a physical iDrive 8 unit is pending.

The formula is adapted from the original [TurnKey E Blend](https://github.com/HasMan/turnkey-ethanol-blend/tree/a378719e9c858ef4693949c3a7bca68bd5f9cafb). The source archive includes the original MIT licence, the MGU Store GPL-3.0-or-later licence and their attribution.
