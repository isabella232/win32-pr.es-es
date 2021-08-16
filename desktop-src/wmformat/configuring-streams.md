---
title: Configuración de Secuencias
description: Configuración de Secuencias
ms.assetid: d119362f-e23c-4985-aff5-8c084106df30
keywords:
- Windows SDK de formato multimedia, secuencias
- profiles,streams
- streams,configuring
- codecs,configuring streams
- profiles,IWMStreamConfig (interfaz)
- streams,IWMStreamConfig (interfaz)
- IWMStreamConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d55db0d02c8eae3ddd3ec780f5d6470d87628a6f7b12feceb5faa413b2e4546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199321"
---
# <a name="configuring-streams"></a>Configuración de Secuencias

Lo único que se requiere en un perfil es al menos una secuencia. Las otras opciones proporcionan acceso a características más avanzadas, pero con el mínimo de una secuencia puede crear un archivo ASF. Es esencial que comprenda cómo configurar secuencias antes de crear perfiles complejos.

Para los perfiles, las secuencias se pueden dividir en dos tipos: los que se comprimen con códecs multimedia de Windows y secuencias arbitrarias que no se procesan con códecs. Las secuencias de audio y las secuencias de vídeo son los tipos que usan los códecs Windows media. Por supuesto, las secuencias pueden contener audio o vídeo comprimido con un códec de terceros, pero el proceso de configuración de dicha secuencia es un caso especial. Para obtener más información, [vea Para crear archivos ASF mediante códecs de terceros.](to-create-asf-files-using-third-party-codecs.md)

En la lista siguiente se resume el proceso de configuración de una secuencia.

1.  Obtenga un objeto de configuración de flujo para la secuencia.
    -   Si va a crear una secuencia mediante uno de los códecs de Windows Media, debe obtener el objeto de configuración de secuencia como formato de códec mediante los métodos de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3).
    -   Si la secuencia es un tipo arbitrario, obtenga un objeto de configuración de secuencia vacío [**mediante IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).
2.  Configure la secuencia para satisfacer sus necesidades.
    -   Secuencias de todos los tipos deben tener asignado un nombre, un nombre de conexión y un número de secuencia.
    -   Secuencias usar Windows códecs multimedia se deben modificar solo de manera predefinida desde el formato de códec. En el caso de las secuencias de audio, solo se debe cambiar la configuración de velocidad de bits variable (VBR) para VBR de dos pases. Las secuencias de vídeo deben configurarse con las propiedades de fotograma deseadas.
    -   Las secuencias arbitrarias tienen distintos requisitos de configuración por tipo. Todos requieren una velocidad de bits y una ventana de búfer.
3.  Agregue la secuencia al perfil mediante una llamada [**a IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream).

Todas las secuencias se definen mediante objetos de configuración de flujo. La interfaz principal de un objeto de configuración de flujo es [**IWMStreamConfig,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)que proporciona métodos para establecer la configuración básica de una secuencia, como el número de secuencia, la velocidad de bits, y así sucesivamente. **IWMStreamConfig** se hereda mediante las interfaces más recientes, [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) e [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3). Al igual que con todas las revisiones de interfaz numeradas, siempre debe recuperar la versión más reciente mediante el **método QueryInterface.**

Se accede a la mayoría de los valores de una secuencia a través [**de IWMMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) Esta configuración se encapsula en una [**estructura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Para audio y vídeo, la estructura **WM \_ MEDIA \_ TYPE** apunta a otra estructura con información adicional específica del tipo de medio. Esta estructura secundaria suele ser [**DESATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) para audio y [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para vídeo. Además, las secuencias de vídeo tienen una estructura terciaria, **BITMAPINFOHEADER,** que describe las características de un fotograma individual de vídeo. **BITMAPINFOHEADER** es una estructura común y se puede encontrar en la sección Interfaz de dispositivo gráfico (GDI) del SDK de plataforma.

En las secciones siguientes se describe cómo configurar secuencias.



| Sección                                                                                                          | Descripción                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración común a todas las Secuencias](configuration-common-to-all-streams.md)                                   | Describe la configuración básica del flujo común a todos los tipos de secuencias.                                                                                        |
| [Obtención de información de configuración de secuencias de códecs](getting-stream-configuration-information-from-codecs.md) | Describe cómo obtener información de configuración de secuencias de los códecs para garantizar la correcta configuración de las secuencias mediante los códecs de audio y vídeo multimedia Windows multimedia. |
| [Configuración de audio Secuencias](configuring-audio-streams.md)                                                       | Describe cómo configurar secuencias de audio.                                                                                                                       |
| [Configuración de video Secuencias](configuring-video-streams.md)                                                       | Describe cómo configurar secuencias de vídeo.                                                                                                                       |
| [Configuración de vídeo Secuencias para buscar rendimiento](configuring-video-streams-for-seeking-performance.md)       | Describe cómo configurar secuencias de vídeo para las que es importante la búsqueda eficaz.                                                                              |
| [Configuración de la captura de pantalla Secuencias](configuring-screen-capture-streams.md)                                     | Describe cómo configurar secuencias de vídeo para la captura de pantalla.                                                                                                    |
| [Configuración de imágenes Secuencias](configuring-image-streams.md)                                                       | Describe cómo configurar secuencias de imágenes.                                                                                                                       |
| [Uso de audio y vídeo sin comprimir Secuencias](using-uncompressed-audio-and-video-streams.md)                     | Describe cómo configurar una secuencia de audio o vídeo sin comprimir.                                                                                                  |
| [Configuración de tipos de secuencia arbitrarios](configuring-arbitrary-stream-types.md)                                     | Describe cómo configurar secuencias para usar los tipos de secuencia arbitrarios predefinidos.                                                                                |
| [Configuración de vbr Secuencias](configuring-vbr-streams.md)                                                           | Describe cómo configurar secuencias para usar la codificación de velocidad de bits variable (VBR).                                                                                     |
| [Configuración de extensiones de unidades de datos](configuring-data-unit-extensions.md)                                         | Describe cómo configurar un flujo para que se puedan adjuntar extensiones de unidad de datos cuando se escribe el archivo.                                                      |
| [Volver a la utilización de configuraciones de flujo](reusing-stream-configurations.md)                                               | Describe las formas en que puede usar objetos de configuración de secuencias de perfiles existentes para crear perfiles nuevos.                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 