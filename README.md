# TurnKey E Blend for iDrive 8

TurnKey E Blend calculates how much petrol and E85 to add to reach a target ethanol percentage when filling the tank. The interface is in English and uses litres. Enter the fuel values manually.

## Install or update in MGU Store

1. Open **Settings → Add source** in MGU Store and enter `vecyoroleg-lgtm/turnkey-e-blend-id8`.
2. Choose **Releases**. You can also add the [HTTPS catalogue](https://raw.githubusercontent.com/vecyoroleg-lgtm/turnkey-e-blend-id8/main/catalog.json) as a source.
3. Select **TurnKey E Blend → Install**. If the app is already installed, select **Update**. Restart iDrive if MGU Store prompts you.

## Calculate a blend

Open **TurnKey E Blend** from the iDrive app menu. Enter the tank capacity, the fuel remaining in the tank, the ethanol percentages of the fuel in the tank and both fuels at the pump, and the target percentage. Select **Save** after each entry, then select **Calculate**. You can leave **Ethanol in tank** blank when the tank is empty.

The result shows the litres of petrol and E85 to add. If the target is outside the range you can reach by filling the tank, the app displays that range. Values stay available while the app is running. The result depends on the fuel percentages and volumes you enter.

## Source code and USB build

Download the [version 0.1.1 source archive](https://github.com/vecyoroleg-lgtm/turnkey-e-blend-id8/blob/main/TurnKey-E-Blend-ID8-0.1.1-GitHub.zip). To build the USB package, extract the archive alongside the [pinned MGU Store source](https://github.com/robertnisipeanu/mgu-store/tree/7dffddd8c3d9efe171f790beb37aba36c41e062e) in a directory named `mgu-store` and run `python build.py` from the app directory with Python 3.9+ and Node.js 18+ available. The build writes `TurnKey-E-Blend-ID8-0.1.1-USB.zip` to `dist`.

Extract the USB archive so `mgu-repo` sits at the root of the drive. Plug it into a data USB port and open **USB** in MGU Store to install. MGU Store builds the native app using the head unit's SDK.

Version 0.1.1 is a beta. The calculation and simulated iDrive screens have been tested locally. Testing on a physical iDrive 8 unit is pending.

The formula is adapted from the original [TurnKey E Blend](https://github.com/HasMan/turnkey-ethanol-blend/tree/a378719e9c858ef4693949c3a7bca68bd5f9cafb). The source archive includes the original MIT licence, the MGU Store GPL-3.0-or-later licence and their attribution.
