---
title: Características agregadas en el SDK de Windows Media 9,5
description: Características agregadas en el SDK de Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, interfaz para el procesamiento específico de la aplicación
- Windows Media Format SDK, DirectX video Acceleration (DXVA)
- SDK de Windows Media Format, interfaz IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versiones basadas en x64 de Windows
- Windows Media Format SDK, códec de imagen de Windows Media Video
- Windows Media Format SDK, códecs de audio
- Windows Media Format SDK, DRM 10 para dispositivos de red
- SDK de Windows Media Format, licencias de DRM
- Windows Media Format SDK, códec de perfil avanzado
- Windows Media Format SDK, formato de interconexión digital de Sony/Philips (S/PDIF)
- SDK de Windows Media Format, formatos de retraso bajo
- SDK de Windows Media Format, modo de búsqueda aproximado
- SDK de Windows Media Format, grabación de listas de reproducción
- SDK de Windows Media Format, compatibilidad con varios idiomas
- Windows Media Format SDK, Windows Media Administrador de dispositivos SDK
- SDK de Windows Media Format, interfaces de códec
- códecs, imagen de Windows Media Video
- Administración de derechos digitales (DRM), protocolo de transferencia segura de dispositivos de red
- DRM (administración de derechos digitales), protocolo de transferencia segura de dispositivos de red
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- códecs, códec de perfil avanzado
- Formato de interconexión digital de Sony/Philips (S/PDIF), transferencia o transmisión con
- S/PDIF (formato Sony/Philips digital Interconnect), transferencia o transmisión con
- modo de búsqueda aproximado
- metadatos, compatibilidad con varios idiomas
- SDK de Administrador de dispositivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149104"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Características agregadas en el SDK de Windows Media 9,5

El SDK de Windows Media Format 9,5 presentó nuevas características para proporcionar una mayor seguridad y flexibilidad en el contenido. Se realizaron los siguientes cambios en el SDK desde la versión 9 series.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nueva interfaz para el procesamiento específico de la aplicación durante la aceleración de vídeo de DirectX

Las aplicaciones de reproductor compatibles con la aceleración de vídeo de DirectX ahora pueden implementar la interfaz [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para realizar el procesamiento específico de la aplicación durante la descodificación de DirectX. El lector llama al método de devolución de llamada [**IWMPLayerHook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de pasar muestras de vídeo comprimidos al procesador de vídeo para la descodificación.

> [!Note]  
> Para usar la interfaz **IWMPlayerHook** y la interfaz [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) asociada, debe tener instalado el número de actualización 888656 en el SDK de Windows Media Format. Puede descargar la actualización desde el [sitio web de Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Versión del SDK de Windows Media Format para versiones basadas en x64 de Windows

Hay disponible una versión basada en x64 del SDK de Windows Media Format. Esta documentación se aplica tanto a las versiones de 32 bits como a la versión basada en x64 del SDK. Sin embargo, no se admite la administración de derechos digitales (DRM) en el SDK de Windows Media Format basado en x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nueva versión del códec de imagen de Windows Media Video

El códec Windows Media Video 9 Image V2 simplifica los cálculos de geometría de ejemplo para la panorámica y el zoom. El nuevo códec también admite varias transiciones complejas entre imágenes.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nueva versión de los códecs de Windows Media Audio

El SDK de Windows Media Format 9,5 incluye los siguientes códecs de audio actualizados:

-   Windows Media Audio 9,1
-   Windows Media Audio 9,1 Professional
-   Windows Media Audio 9,1 Lossless

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Compatibilidad del Protocolo de Windows Media DRM 10 con dispositivos de red

El SDK de Windows Media Format 9,5 admite el nuevo protocolo de transferencia segura de Windows Media DRM 10 para dispositivos de red. Este protocolo se puede usar para transmitir contenido cifrado a través de una red local a un dispositivo de reproducción, como un receptor de vídeo de un conjunto.

La mayoría de los procedimientos que se usan para implementar la compatibilidad con Windows Media DRM 10 para dispositivos de red deben ser realizados por la aplicación. Sin embargo, puede usar los métodos del SDK de Windows Media Format para proporcionar la siguiente funcionalidad:

-   Mantener una base de datos de dispositivos, incluidos los que están habilitados para Windows Media DRM 10 para dispositivos de red.
-   Valide los dispositivos para asegurarse de que estén lo suficientemente cerca del cliente en la red para la transmisión por secuencias segura.
-   Convertir archivos protegidos con DRM en Windows Media DRM 10 para transmisiones de dispositivos de red.
-   Escribir archivos con datos cifrados previamente.

## <a name="support-for-new-drm-licenses"></a>Compatibilidad con nuevas licencias de DRM

Las nuevas licencias creadas con el SDK de Windows Media Rights Manager usan niveles de protección de salida (OPLs) para especificar derechos y restricciones para reproducir y copiar contenido. El SDK de Windows Media Format proporciona compatibilidad para leer el OPLs de una licencia.

## <a name="new-video-codec"></a>Nuevo códec de vídeo

El códec de perfil avanzado de Windows Media Video 9 se basa en la alta calidad del códec de Windows Media Video 9 al agregar compatibilidad con la codificación entrelazada.

## <a name="spdif-output"></a>Salida S/PDIF

El contenido codificado con uno de los códecs profesionales de Windows Media Audio se puede transferir o transmitir mediante el formato de interconexión digital de Sony/Philips (S/PDIF).

## <a name="low-delay-audio"></a>Low-Delay audio

Los códecs Professional Windows Media Audio 9,1 y Windows Media Audio 9,1 ahora admiten varios formatos de retraso bajo. Estos formatos producen secuencias de audio que se pueden iniciar más rápidamente, lo que reduce la latencia en escenarios de cambio de secuencia. La latencia general de las difusiones en vivo también se ha mejorado mediante el uso de formatos de retraso reducido.

## <a name="approximate-seeking-mode"></a>Modo de búsqueda aproximado

Ahora puede buscar una hora aproximada en un archivo ASF con el lector. Este modo mejora el rendimiento al realizar una búsqueda imprecisa, como cuando un usuario hace clic en la barra de búsqueda de Windows Media Player. La búsqueda aproximada devuelve el ejemplo multimedia para el cleanpoint anterior en lugar de reconstruir el ejemplo para el tiempo que se busca.

## <a name="playlist-burning"></a>Grabación de listas de reproducción

Windows Media DRM 10 admite derechos para copiar archivos de audio en el CD de libro rojo como parte de una lista de reproducción. El SDK de Windows Media Format proporciona métodos para comprobar si se pueden copiar los archivos de una lista de reproducción.

## <a name="improved-multiple-language-support-for-metadata"></a>Compatibilidad mejorada con Multiple-Language para metadatos

En el SDK de Windows Media Format 9 series, todos los metadatos agregados a un archivo se asignaron a una lista de idiomas que tenía el identificador de idioma del idioma predeterminado. Esto causaba problemas cuando los distribuidores de contenido de diferentes configuraciones regionales agregaban algunos metadatos, ya que los usuarios de la configuración regional del distribuidor solo ven los pocos atributos agregados para su idioma. El SDK de Windows Media Format 9,5 soluciona este problema al no crear una lista de idiomas hasta que haya atributos de dos idiomas presentes en el archivo. En ese momento, todos los metadatos se asocian a la configuración regional del segundo idioma, que luego se convierte en el valor predeterminado. De esta manera, un distribuidor de contenido puede mantener intactos todos los metadatos originales de un archivo, como el título y el autor, al agregar algunos atributos relacionados con su configuración regional.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>SDK de Windows Media Administrador de dispositivos incluido en la instalación

El paquete de instalación del SDK de Windows Media Format 9,5 instala el SDK de Windows Media Administrador de dispositivos. La documentación del SDK de Windows Media Administrador de dispositivos se puede encontrar en la carpeta C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (la carpeta será diferente si no instala el SDK de Windows Media Format en la carpeta predeterminada).

## <a name="codec-interface-documentation"></a>Documentación de la interfaz de códec

En esta documentación se incluye información acerca del uso de los códecs de Windows Media Audio y vídeo fuera del SDK de Windows Media Format. Esta documentación se publicó originalmente como parte de una descarga de Microsoft Developer Network. Las aplicaciones de ejemplo que muestran el uso del códec DMOs directamente se incluyen en la instalación del SDK de Windows Media Format junto con los encabezados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




