---
title: Características agregadas en el SDK Windows Media 9.5
description: Características agregadas en el SDK Windows Media 9.5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows SDK de formato multimedia, características
- Windows SDK de formato multimedia, nuevas características
- Windows SDK de formato multimedia, interfaz para el procesamiento específico de la aplicación
- Windows SDK de formato multimedia, aceleración de vídeo directX (DXVA)
- Windows SDK de formato multimedia, interfaz IWMPlayerHook
- IWMPlayerHook
- Windows SDK de formato multimedia, versiones basadas en x64 de Windows
- Windows SDK de formato multimedia, Windows códec de imagen de vídeo multimedia
- Windows SDK de formato multimedia, códecs de audio
- Windows SDK de formato multimedia, DRM 10 para dispositivos de red
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, códec de perfil avanzado
- Windows Sdk de formato multimedia, formato de interconexión digital de Sony/Digital Digital Desconecto (S/PDIF)
- Windows SDK de formato multimedia, formatos de retraso bajo
- Windows SDK de formato multimedia, modo de búsqueda aproximado
- Windows SDK de formato multimedia, grabación de lista de reproducción
- Windows SDK de formato multimedia, compatibilidad con varios lenguajes
- Windows SDK de formato multimedia, WINDOWS SDK de Administrador de dispositivos multimedia
- Windows SDK de formato multimedia, interfaces de códec
- codecs,Windows imagen de vídeo multimedia
- administración de derechos digitales (DRM),Protocolo de transferencia segura de dispositivos de red
- DRM (administración de derechos digitales),Protocolo de transferencia segura de dispositivos de red
- administración de derechos digitales (DRM),licencias
- DRM (administración de derechos digitales), licencias
- códecs, códec de perfil avanzado
- Formato de interconexión digital (S/PDIF) de Sony/Dfs, transferencia o transmisión mediante
- S/PDIF (formato de interconexión digital de Hanó/Df), transferencia o transmisión mediante
- modo de búsqueda aproximado
- metadata,compatibilidad con varios idiomas
- Windows SDK de Administrador de dispositivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcabd2fd3ae1b1030b04c0be342bcb64678e98eef601c83570ad68a13567820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591405"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Características agregadas en el SDK Windows Media 9.5

El SDK Windows Media Format 9.5 introdujo nuevas características para proporcionar una mayor flexibilidad y seguridad de contenido. Los siguientes cambios se realizaron en el SDK desde la versión de la serie 9.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nueva interfaz para el procesamiento específico de la aplicación durante la aceleración de vídeo de DirectX

Las aplicaciones de reproductor que admiten la aceleración de vídeo de DirectX ahora pueden implementar la interfaz [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para realizar el procesamiento específico de la aplicación durante la decodificación de DirectX VA. El lector llama al método de devolución de llamada [**IWMPLayerHook::P reDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de pasar ejemplos de vídeo comprimidos al procesador de vídeo para descodificar.

> [!Note]  
> Para usar la **interfaz IWMPlayerHook** y la interfaz [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) asociada, debe tener el número de actualización 888656 instalado en el SDK de formato multimedia de Windows. Puede descargar la actualización desde el sitio [web de Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Windows Versión del SDK de formato multimedia para versiones basadas en x64 de Windows

Hay disponible una versión basada en x64 del SDK Windows Media Format. Esta documentación se aplica tanto a las versiones de 32 bits como a la versión basada en x64 del SDK. Sin embargo, la administración de derechos digitales (DRM) no se admite en el SDK de formato multimedia basado Windows x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nueva versión del códec Windows imagen de vídeo multimedia

El códec Windows Media Video 9 Image v2 simplifica los cálculos de geometría de ejemplo para el movimiento panorámico y el zoom. El nuevo códec también admite varias transiciones complejas entre imágenes.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nueva versión de los códecs Windows media audio

El SDK Windows Media Format 9.5 incluye los siguientes códecs de audio actualizados:

-   Windows Audio multimedia 9.1
-   Windows Audio multimedia 9.1 Professional
-   Windows Audio multimedia 9.1 sin pérdida

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Windows Drm multimedia 10 para compatibilidad con el protocolo de dispositivos de red

El SDK Windows Media Format 9.5 admite el nuevo protocolo de transferencia segura Windows Media DRM 10 para dispositivos de red. Este protocolo se puede usar para transmitir contenido cifrado a través de una red local a un dispositivo de reproducción, como un receptor de vídeo establecido en la parte superior.

La aplicación debe realizar la mayoría de los procedimientos usados para implementar la compatibilidad con Windows Drm 10 multimedia para dispositivos de red. Sin embargo, puede usar métodos del SDK Windows Media Format para proporcionar la siguiente funcionalidad:

-   Mantenga una base de datos de dispositivos, incluidos los que están habilitados para Windows DRM 10 multimedia para dispositivos de red.
-   Valide los dispositivos para asegurarse de que están lo suficientemente "cerca" del cliente en la red para el streaming seguro.
-   Convierta los archivos protegidos con DRM en Windows drm multimedia 10 para los flujos de dispositivos de red.
-   Escribir archivos con datos previamente cifrados.

## <a name="support-for-new-drm-licenses"></a>Compatibilidad con nuevas licencias DRM

Las nuevas licencias creadas mediante el SDK de Windows Media Rights Manager usan niveles de protección de salida (OPL) para especificar derechos y restricciones para reproducir y copiar contenido. El SDK Windows Media Format proporciona compatibilidad para leer las OPL de una licencia.

## <a name="new-video-codec"></a>Nuevo códec de vídeo

El códec Windows perfil avanzado de Windows Media Video 9 se basa en la alta calidad del códec Windows Media Video 9, al tiempo que agrega compatibilidad con la codificación entrelazada.

## <a name="spdif-output"></a>Salida de S/PDIF

El contenido codificado con uno de los códecs Professional audio multimedia de Windows ahora se puede transferir o transmitir mediante el formato de interconexión digital de Audio multimedia (S/PDIF).

## <a name="low-delay-audio"></a>Low-Delay Audio

Los códecs Windows Media Audio 9.1 y Windows Media Audio 9. Professional 1 ahora admiten varios formatos de retraso bajo. Estos formatos generan secuencias de audio que se pueden iniciar más rápidamente, lo que reduce la latencia en escenarios de conmutación de secuencias. La latencia general en las retransmisiones en directo también se mejora mediante el uso de formatos de retraso bajo.

## <a name="approximate-seeking-mode"></a>Modo de búsqueda aproximado

Ahora puede buscar una hora aproximada en un archivo ASF con el lector. Este modo mejora el rendimiento al realizar una búsqueda imprecisa, como cuando un usuario hace clic en la barra de búsqueda en Reproductor de Windows Media. La búsqueda aproximada devuelve la muestra de medios para el punto limpio anterior en lugar de reconstruir la muestra durante el tiempo preciso que se busca.

## <a name="playlist-burning"></a>Reproducción de listas de reproducción

Windows Drm multimedia 10 admite derechos para copiar archivos de audio en Red Book CD como parte de una lista de reproducción. El SDK Windows media format proporciona métodos para comprobar si los archivos de una lista de reproducción pueden copiarse.

## <a name="improved-multiple-language-support-for-metadata"></a>Compatibilidad mejorada Multiple-Language de metadatos

En el SDK de Windows Media Format 9, todos los metadatos agregados a un archivo se asignaron a una lista de idiomas a la que se le asignó el identificador de idioma del idioma predeterminado. Esto produjo problemas cuando los distribuidores de contenido de diferentes configuraciones regionales agregaron algunos metadatos, ya que los usuarios de la configuración regional del distribuidor solo ven los pocos atributos agregados para su idioma. El SDK Windows Media Format 9.5 soluciona este problema al no crear una lista de idiomas hasta que haya atributos de dos idiomas presentes en el archivo. En ese momento, todos los metadatos están asociados a la configuración regional del segundo idioma, que luego se convierte en el valor predeterminado. De esta manera, un distribuidor de contenido puede mantener intactos todos los metadatos originales de un archivo, como el título y el autor, al tiempo que agrega algunos atributos pertinentes a su configuración regional.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Windows SDK Administrador de dispositivos multimedia incluido en la instalación

El paquete de instalación del SDK Windows Media Format 9.5 instala el SDK Windows Media Administrador de dispositivos SDK. La documentación del SDK de Windows Media Administrador de dispositivos se puede encontrar en la carpeta de documentos C: \\ WMSDK \\ WMFSDK95 \\ WMDM (la carpeta será diferente si no instala el SDK de formato multimedia de Windows en la carpeta \\ predeterminada).

## <a name="codec-interface-documentation"></a>Documentación de la interfaz de códec

En esta documentación se incluye información sobre el uso Windows códecs de audio y vídeo multimedia fuera del SDK Windows Media Format. Esta documentación se publicó originalmente como parte de una descarga de Desarrollador de Microsoft Network. Las aplicaciones de ejemplo que muestran cómo usar las DDO de códec directamente se incluyen en la instalación del SDK Windows Media Format junto con los encabezados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




