---
title: Configuración de secuencias
description: Configuración de secuencias
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows Media Format SDK, secuencias
- perfiles, secuencias
- flujos, configurar
- códecs, configurar secuencias
- perfiles, interfaz IWMStreamConfig
- streams, interfaz IWMStreamConfig
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc159fbd5390eb430e035db676685153d0cf174
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487727"
---
# <a name="configuring-streams"></a>Configuración de secuencias

Lo único que se necesita en un perfil es al menos un flujo. Las demás opciones proporcionan acceso a características más avanzadas, pero con el mínimo de una secuencia, puede crear un archivo ASF. Es importante que comprenda cómo configurar transmisiones antes de crear perfiles complejos.

Para los perfiles, las secuencias se pueden dividir en dos tipos: los que se comprimen con códecs de Windows Media y secuencias arbitrarias que no se procesan con ningún códec. Los flujos de audio y las secuencias de vídeo son los tipos que usan los códecs de Windows Media. Por supuesto, las secuencias pueden contener audio o vídeo comprimido con un códec de otro fabricante, pero el proceso de configuración de este tipo de flujo es un caso especial. Para obtener más información, vea [para crear archivos ASF con códecs de terceros](to-create-asf-files-using-third-party-codecs.md).

En la lista siguiente se resume el proceso de configuración de una secuencia.

1.  Obtenga un objeto de configuración de secuencia para la secuencia.
    -   Si va a crear una secuencia con uno de los códecs de Windows Media, debe obtener el objeto de configuración de la secuencia como un formato de códec mediante los métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3).
    -   Si el flujo es un tipo arbitrario, obtenga un objeto de configuración de secuencia vacío mediante [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configure el flujo para satisfacer sus necesidades.
    -   A los flujos de todos los tipos se les debe asignar un nombre, un nombre de conexión y un número de secuencia.
    -   Los flujos que usan códecs de Windows Media solo se deben modificar de forma predefinida en el formato del códec. En el caso de las secuencias de audio, se debe cambiar la configuración de velocidad de bits variable (VBR) para VBR de dos pasos. Las secuencias de vídeo deben configurarse con las propiedades de fotogramas deseadas.
    -   Los flujos arbitrarios tienen requisitos de configuración diferentes por tipo. Todos requieren una ventana de velocidad de bits y de búfer.
3.  Agregue la secuencia al perfil llamando a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Todas las secuencias se definen mediante objetos de configuración de secuencia. La interfaz principal de un objeto de configuración de secuencia es [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig), que proporciona métodos para establecer la configuración básica de una secuencia, como el número de secuencia, la velocidad de bits, etc. **IWMStreamConfig** es heredado por las interfaces más recientes, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) y [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Como con todas las revisiones de interfaz numeradas, siempre debe recuperar la versión más reciente mediante el método **QueryInterface** .

Se tiene acceso a la mayoría de los valores de una secuencia a través de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). Estos valores se encapsulan en una estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . En audio y vídeo, la estructura de **\_ \_ tipo de medio de WM** apunta a otra estructura con más información específica del tipo de medio. Esta estructura secundaria suele ser [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) para audio y [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para vídeo. Además, las secuencias de vídeo tienen una estructura terciaria, **BITMAPINFOHEADER**, que describe las características de un fotograma individual de vídeo. **BITMAPINFOHEADER** es una estructura común y se puede encontrar en la sección interfaz de dispositivo gráfico (GDI) del SDK de la plataforma.

En las secciones siguientes se describe cómo configurar las secuencias.



| Sección                                                                                                          | Descripción                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración común para todos los flujos](configuration-common-to-all-streams.md)                                   | Describe la configuración básica de la secuencia común a todos los tipos de secuencias.                                                                                        |
| [Obtención de información de configuración de la secuencia de códecs](getting-stream-configuration-information-from-codecs.md) | Describe cómo obtener la información de configuración de la secuencia de los códecs para garantizar la correcta configuración de las secuencias mediante los códecs de Windows Media Audio y vídeo. |
| [Configuración de secuencias de audio](configuring-audio-streams.md)                                                       | Describe cómo configurar secuencias de audio.                                                                                                                       |
| [Configuración de secuencias de vídeo](configuring-video-streams.md)                                                       | Describe cómo configurar secuencias de vídeo.                                                                                                                       |
| [Configuración de secuencias de vídeo para buscar rendimiento](configuring-video-streams-for-seeking-performance.md)       | Describe cómo configurar secuencias de vídeo para las que es importante una búsqueda eficaz.                                                                              |
| [Configurar secuencias de captura de pantalla](configuring-screen-capture-streams.md)                                     | Describe cómo configurar secuencias de vídeo para la captura de pantalla.                                                                                                    |
| [Configuración de secuencias de imágenes](configuring-image-streams.md)                                                       | Describe cómo configurar secuencias de imágenes.                                                                                                                       |
| [Uso de secuencias de audio y vídeo sin comprimir](using-uncompressed-audio-and-video-streams.md)                     | Describe cómo configurar una secuencia de audio o vídeo sin comprimir.                                                                                                  |
| [Configuración de tipos de flujo arbitrarios](configuring-arbitrary-stream-types.md)                                     | Describe cómo configurar secuencias para usar los tipos de secuencia arbitrarios predefinidos.                                                                                |
| [Configuración de secuencias VBR](configuring-vbr-streams.md)                                                           | Describe cómo configurar secuencias para usar la codificación de velocidad de bits (VBR) variable.                                                                                     |
| [Configuración de extensiones de unidades de datos](configuring-data-unit-extensions.md)                                         | Describe cómo configurar una secuencia para que las extensiones de unidad de datos se puedan adjuntar al escribir el archivo.                                                      |
| [Reutilizar configuraciones de secuencia](reusing-stream-configurations.md)                                               | Describe las formas en que puede utilizar los objetos de configuración de la secuencia de los perfiles existentes para crear perfiles nuevos.                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 