---
title: Novedades del Reproductor de Windows Media 11
description: En este tema se enumeran las características nuevas de Reproductor de Windows Media 11 y el SDK Reproductor de Windows Media 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Reproductor de Windows Media, novedades
- Reproductor de Windows Media,nuevas características
- kit de desarrollo de software (SDK),Reproductor de Windows Media 11
- SDK (kit de desarrollo de software), Reproductor de Windows Media 11
- documentation,Reproductor de Windows Media SDK 11
- novedades, Reproductor de Windows Media 11
- nuevas características, Reproductor de Windows Media 11
- interfaces,nuevas características de Reproductor de Windows Media 11
- atributos,nuevas características de Reproductor de Windows Media 11
- Reproductor de Windows Media ActiveX, nuevas características de la versión 11
- ActiveX, nuevas características de la versión 11
- máscaras, nuevas características de Reproductor de Windows Media 11
- Reproductor de Windows Media máscaras, nuevas características de la versión 11
- complementos, nuevas características de Reproductor de Windows Media 11
- Reproductor de Windows Media complementos, nuevas características de la versión 11
- tiendas en línea, nuevas características de Reproductor de Windows Media 11
- Reproductor de Windows Media en línea, nuevas características de la versión 11
- samples,new features in Reproductor de Windows Media 11
- versiones de Reproductor de Windows Media,nuevas características de la versión 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69f9ffdeb3325b7b993e3c2a1826567ebd5507f4d0290248ad4c570b788e137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001275"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Novedades del Reproductor de Windows Media 11

En este tema se enumeran las características nuevas de Reproductor de Windows Media 11 y el SDK Reproductor de Windows Media 11.

## <a name="windows-media-player-control"></a>Reproductor de Windows Media Control

Las interfaces siguientes eran nuevas en el control Reproductor de Windows Media 11 ActiveX 11.

-   [**IWMPLibrary (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**IWMPLibraryServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**IWMPLibrarySharingServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2 (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**IWMPQuery (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**IWMPStringCollection2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Objeto MediaCollection**](mediacollection-object.md)
-   [**Objeto Query**](query-object.md)
-   [**StringCollection (objeto)**](stringcollection-object.md)
-   [**IWMPCdromRip (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**IWMPCdromRom Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**IWMPFolderMonitorServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPSyncDevice2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig (interfaz)**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**IWMPEvents3 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Reproductor de Windows Media Pieles

Las siguientes características de máscara eran nuevas en Reproductor de Windows Media 11.

-   Nuevos atributos para los controles de posicionamiento. Vea [**AmbientAttributes.right**](ambientattributes-right.md) y [**AmbientAttributes.bottom.**](ambientattributes-bottom.md)
-   Nuevos atributos para mover y cambiar el tamaño de los controles. Vea [**AmbientAttributes.moveSizeTo**](ambientattributes-movesizeto.md) y [**AmbientAttributes.slideTo**](ambientattributes-slideto.md).
-   Nuevo atributo para especificar el comportamiento de cambio de tamaño de la imagen. Vea [**AmbientAttributes.resizeImages.**](ambientattributes-resizeimages.md)
-   Nuevo atributo para especificar el escalado no uniforme de un elemento de máscara. Vea [**AmbientAttributes.nineGridMargins.**](ambientattributes-ninegridmargins.md)

## <a name="windows-media-player-plug-ins"></a>Reproductor de Windows Media Complementos

El SDK Reproductor de Windows Media 11 introdujo un nuevo tipo de complemento para convertir formatos de archivo multimedia digitales. Vea [Reproductor de Windows Media conversion plug-ins (Complementos de conversión de archivos).](windows-media-player-conversion-plug-ins.md)

Los complementos de DSP creados antes del lanzamiento del SDK Reproductor de Windows Media 11 deben actualizarse para que funcionen con Reproductor de Windows Media 11. Consulte [Actualización de los complementos DE DSP existentes.](updating-existing-dsp-plug-ins.md)

El Reproductor de Windows Media complemento se actualizó para crear complementos DSP que funcionen en Reproductor de Windows Media 11. Para obtener más información, vea [Updates to the DSP Plug-in Wizard for Reproductor de Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Reproductor de Windows Media Tiendas en línea

Reproductor de Windows Media 11 introdujo un nuevo modelo para integrar catálogos de tiendas en línea en la característica Reproductor de Windows Media biblioteca. Vea [Type 1 Online Stores](type-1-online-stores.md).

## <a name="windows-media-player"></a>Reproductor de Windows Media

Las siguientes características eran nuevas en Reproductor de Windows Media 11.

-   [Extensiones de dispositivo para notificar contenido adquirido](device-extensions-for-reporting-acquired-content.md)
-   [Extensiones de dispositivo para las preferencias de objetos de lista de reproducción](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Reproductor de Windows Media Ejemplos del SDK

El ejemplo de C# denominado SchemaReader era nuevo en el SDK Reproductor de Windows Media 11. El ejemplo crea una herramienta que usa el modelo de objetos Reproductor de Windows Media para recuperar y mostrar información sobre los metadatos en la biblioteca Reproductor de Windows Media o en un archivo multimedia digital. La herramienta puede guardar los resultados en un archivo de texto. La herramienta enumera los nombres de atributo de metadatos almacenados en la biblioteca para cada esquema admitido (audio, vídeo, lista de reproducción, foto y otros). La herramienta también puede proporcionar información sobre los atributos disponibles para las listas de reproducción en la colección de listas de reproducción, pistas de CD, tabla de contenido de CD, títulos de DVD, capítulos de DVD, tabla de contenido de DVD y archivos multimedia individuales.

El ejemplo de C++ denominado WMPML se actualizó en el SDK Reproductor de Windows Media 11 para mostrar las siguientes características:

-   Uso de la [**nueva interfaz IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) para crear una interfaz de usuario similar a la característica Reproductor de Windows Media biblioteca.
-   Usar las [**interfaces IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) [**e IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) para crear consultas compuestas y mostrar los resultados.

 

 




