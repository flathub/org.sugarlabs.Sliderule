# Slideruler Activity Flatpak

To know more refer https://github.com/sugarlabs/slideruler

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Sliderule.git
cd org.sugarlabs.Sliderule
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.Sliderule.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Sliderule
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Sliderule.json
```