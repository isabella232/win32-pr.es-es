---
title: Novedades del Reproductor de Windows Media 11
description: En este tema se enumeran las características nuevas de Windows Media Player 11 y el SDK de Windows Media Player 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player, novedades
- Windows Media Player, nuevas características
- Kit de desarrollo de software (SDK), Windows Media Player 11
- SDK (kit de desarrollo de software), Windows Media Player 11
- documentación, SDK de Windows Media Player 11
- novedades, Windows Media Player 11
- nuevas características, Windows Media Player 11
- interfaces, nuevas características de Windows Media Player 11
- atributos, nuevas características de Windows Media Player 11
- Control ActiveX de Windows Media Player, nuevas características de la versión 11
- Control ActiveX, nuevas características de la versión 11
- máscaras, nuevas características de Windows Media Player 11
- Aspectos de Windows Media Player, nuevas características de la versión 11
- complementos, nuevas características de Windows Media Player 11
- Complementos de Windows Media Player, nuevas características de la versión 11
- tiendas en línea, nuevas características de Windows Media Player 11
- Windows Media Player tiendas en línea, nuevas características de la versión 11
- ejemplos, nuevas características de Windows Media Player 11
- versiones de Windows Media Player, nuevas características de la versión 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077445"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Novedades del Reproductor de Windows Media 11

En este tema se enumeran las características nuevas de Windows Media Player 11 y el SDK de Windows Media Player 11.

## <a name="windows-media-player-control"></a>Control de Media Player de Windows

Las siguientes interfaces eran nuevas en el control ActiveX de Windows Media Player 11.

-   [**Interfaz IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interfaz IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interfaz IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interfaz IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interfaz IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interfaz IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Objeto MediaCollection**](mediacollection-object.md)
-   [**Query (objeto)**](query-object.md)
-   [**StringCollection (objeto)**](stringcollection-object.md)
-   [**Interfaz IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interfaz IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interfaz IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interfaz IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interfaz IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**Interfaz IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Máscaras de Windows Media Player

Las siguientes características de máscara eran nuevas en Windows Media Player 11.

-   Nuevos atributos para colocar controles. Vea [**AmbientAttributes. Right**](ambientattributes-right.md) y [**AmbientAttributes. Bottom**](ambientattributes-bottom.md).
-   Nuevos atributos para mover y cambiar el tamaño de los controles. Vea [**AmbientAttributes. moveSizeTo**](ambientattributes-movesizeto.md) y [**AmbientAttributes. slideto**](ambientattributes-slideto.md).
-   Nuevo atributo para especificar el comportamiento de cambio de tamaño de la imagen. Vea [**AmbientAttributes. resizeImages**](ambientattributes-resizeimages.md).
-   Nuevo atributo para especificar el escalado no uniforme de un elemento de máscara. Vea [**AmbientAttributes. nineGridMargins**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Complementos de Media Player de Windows

El SDK de Windows Media Player 11 presentó un nuevo tipo de complemento para convertir formatos de archivos multimedia digitales. Consulte [Complementos de conversión de Windows Media Player](windows-media-player-conversion-plug-ins.md).

Los complementos DSP creados antes de la versión del SDK de Windows Media Player 11 deben actualizarse para que funcionen con Windows Media Player 11. Consulte [actualización de complementos de DSP existentes](updating-existing-dsp-plug-ins.md).

El Asistente para complementos de Windows Media Player se actualizó para crear complementos de DSP que funcionan en Windows Media Player 11. Para obtener más información, consulte [actualizaciones del Asistente para complementos de DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Windows Media Player tiendas en línea

Windows Media Player 11 presentó un nuevo modelo para la integración de catálogos de tiendas en línea en la característica biblioteca de Media Player de Windows. Vea las [tiendas en línea de tipo 1](type-1-online-stores.md).

## <a name="windows-media-player"></a>Reproductor de Windows Media

Las siguientes características son nuevas en Windows Media Player 11.

-   [Extensiones de dispositivo para la generación de informes de contenido adquirido](device-extensions-for-reporting-acquired-content.md)
-   [Extensiones de dispositivo para preferencias de objetos de lista de reproducción](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Ejemplos del SDK de Windows Media Player

El ejemplo de C# denominado SchemaReader era nuevo en el SDK de Windows Media Player 11. En el ejemplo se crea una herramienta que usa el modelo de objetos de Media Player de Windows para recuperar y Mostrar información sobre los metadatos de la biblioteca de Media Player de Windows o en un archivo multimedia digital. La herramienta puede guardar los resultados en un archivo de texto. La herramienta enumera los nombres de los atributos de metadatos almacenados en la biblioteca para cada esquema admitido (audio, vídeo, lista de reproducción, Foto y otros). La herramienta también puede proporcionar información acerca de los atributos disponibles para listas de reproducción en la colección de listas de reproducción, pistas de CD, tabla de CD de contenido, títulos de DVD, capítulos de DVD, tabla de DVD de contenido y archivos multimedia individuales.

El ejemplo de C++ denominado WMPML se actualizó en el SDK de Windows Media Player 11 para mostrar las características siguientes:

-   El uso de la nueva interfaz [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) para crear una interfaz de usuario similar a la de la característica Biblioteca Media Player de Windows.
-   Usar las interfaces [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) y [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) para crear consultas compuestas y mostrar los resultados.

 

 




