---
title: Habilitación de la aceleración de vídeo de DirectX
description: Habilitación de la aceleración de vídeo de DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows SDK de formato multimedia, habilitación de DXVA
- Windows SDK de formato multimedia, aceleración de vídeo directX (DXVA)
- Windows SDK de formato multimedia, aceleración de vídeo
- Formato de sistemas avanzados (ASF), habilitar DXVA
- ASF (formato de sistemas avanzados), habilitar DXVA
- Advanced Systems Format (ASF), DirectX Video Acceleration (DXVA)
- ASF (formato de sistemas avanzados), aceleración de vídeo DirectX (DXVA)
- Formato de sistemas avanzados (ASF), aceleración de vídeo
- ASF (formato de sistemas avanzados), aceleración de vídeo
- Aceleración de vídeo de DirectX (DXVA), habilitación
- DXVA (aceleración de vídeo de DirectX), habilitar
- Aceleración de vídeo de DirectX (DXVA), orden de las operaciones
- DXVA (aceleración de vídeo de DirectX), orden de las operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840549c9a148fdfe8cc67daf46645ffb0925369057fe71f0c17217bfd36823ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930768"
---
# <a name="enabling-directx-video-acceleration"></a>Habilitación de la aceleración de vídeo de DirectX

En esta sección se describe cómo habilitar Microsoft® DirectX® aceleración de vídeo al reproducir contenido transmitido en un reproductor personalizado.

## <a name="background"></a>Información previa

DirectX Video Acceleration (DirectX VA) es una especificación de API para la aceleración de hardware de las operaciones decodización 2D. Permite a los descodificadores de software descargar determinadas operaciones que consumen mucha CPU en la tarjeta gráfica para su procesamiento. Para los usuarios finales, esto hace posible vídeo de alta velocidad de bits, como la reproducción de DVD de pantalla completa en equipos antiguos equipados con tarjetas gráficas compatibles con DirectX VA.

A partir del SDK Windows Media Format 9 Series, el filtro DMO Wrapper admite DirectX VA. Esto significa que, para la reproducción local, las aplicaciones pueden usar el filtro wm ASF Reader para reproducir contenido basado en medios de Windows y la aceleración de hardware de DirectX VA se invocará automáticamente si la tarjeta gráfica lo admite. Sin embargo, el filtro WM ASF Reader no admite la reproducción de contenido transmitido por secuencias. Por lo tanto, si desea admitir DirectX VA al reproducir contenido transmitido en un reproductor personalizado, debe usar un mecanismo alternativo, que es el que usa Reproductor de Windows Media a partir de la serie Windows Media 9.

Como Reproductor de Windows Media se diseñó antes de que se desarrollaron los filtros QASF, Reproductor de Windows Media tiene su propio filtro de origen, basado en el SDK de formato multimedia de Windows, para reproducir contenido basado en Windows multimedia. El filtro de origen Windows multimedia WMP entrega datos descomprimidos de bajada directamente a los representadores de audio y vídeo. Por el contrario, el lector ASF de WM entrega contenido comprimido de bajada a los objetos multimedia DirectX (DMO) del descodificador de medios de Windows, que se hospedan dentro del contenedor de DMO. En los diagramas siguientes se muestran las diferencias entre el lector de ASF de WM y el filtro de origen de Windows WMP.

![ejemplos sin comprimir de salida de filtro de origen personalizado](images/wmp-dxva-graph.png)

![Salidas de filtro de origen qasf ejemplos comprimidos](images/qasf-dxva-graph.png)

Para habilitar DirectX VA para el contenido transmitido, debe crear un filtro de origen personalizado como el del diagrama superior. Básicamente, este filtro usará el SDK de formato multimedia de Windows para crear instancias de un objeto de lector WM, descomprimir los ejemplos y enviarlos de bajada en sus pines de salida. En esta explicación se da por supuesto que ya ha creado el filtro de origen y que ahora está listo para implementar la compatibilidad con DirectX VA.

Para habilitar DirectX VA, la tarea básica del filtro de origen es proporcionar el representador de vídeo y el descodificador WMV DMO con las interfaces que necesitarán para negociar la conexión de Va de DirectX. El filtro de origen no participa en esas negociaciones. Una vez que se inicia el streaming, la única tarea relacionada con DirectX VA que puede realizar el filtro de origen es modificar las marcas de tiempo en los ejemplos de vídeo antes de que el descodificador WMV las entregue al representador de vídeo. La razón principal para hacerlo es proporcionar control de escala de tiempo personalizado más allá de lo que habilitan las interfaces DirectShow® estándar.

Se definen tres interfaces para habilitar las comunicaciones necesarias entre el SDK de formato multimedia de Windows, el filtro de origen del reproductor, el descodificador de vídeo multimedia de Windows DMO y el Mixer de superposición o el representador de mezcla de vídeo. Estas interfaces se describen en la tabla siguiente.



| Interfaz                                                        | Descripción                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Expuesto por Windows Media Decoder DMO y llamado por el filtro de origen de un reproductor multimedia para configurar las distintas conexiones necesarias para habilitar DirectX VA para descodificar contenido de Windows Media Video. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Se implementa en el filtro de origen del reproductor. Permite que el filtro modifique las marcas de tiempo en los ejemplos de vídeo antes de entregarlas de bajada.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Se implementa en el objeto WM Reader. Lo llama un filtro de origen del reproductor para obtener interfaces del descodificador DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Orden de las operaciones en la reproducción habilitada para DIRECTX VA

En esta sección se describe el orden general de las operaciones en tiempo de ejecución para un reproductor habilitado para VA de DirectX y su filtro de origen. Los componentes a los que se hace referencia en esta sección son:

-   Un reproductor multimedia de terceros, denominado reproductor.
-   Filtro de origen personalizado, creado por el reproductor, que usa el SDK de formato multimedia de Windows para descomprimir Windows contenido basado en multimedia.
-   El pin de salida de vídeo del filtro de origen del reproductor, denominado pin de salida.
-   El DirectShow de filtro de reproducción de vídeo, denominado gráfico.
-   Representador de mezcla de vídeo, denominado VMR.
-   El Windows lector asincrónico del SDK de formato multimedia, denominado lector.
-   El Windows multimedia del descodificador de vídeo multimedia DirectX, denominado descodificador DMO.

El orden de las operaciones es el siguiente:

1.  El reproductor crea instancias de su filtro de origen y un objeto de lector. El lector crea un descodificador de vídeo DMO establece el tipo de entrada (comprimido) en él. Esto debe ocurrir antes de que el reproductor intente configurar su gráfico de reproducción de vídeo porque el SDK y el descodificador DMO deben estar implicados en el proceso de negociación con el gráfico y el DMO debe conocer el formato de entrada durante el paso 9.
2.  El reproductor llama **a IGraphBuilder::Render,** lo que le proporciona el pin de salida del filtro de origen de vídeo. En este punto, el administrador DirectShow gráfico de filtros intenta conectar el VMR al filtro de origen de vídeo del reproductor.
3.  El administrador de gráficos de filtros llama a **IPin::Conectar** en el pin de salida del filtro de origen de vídeo del reproductor.

Los pasos del 4 al 10 se producen dentro de **IPin::Conectar**.

1.  El filtro de origen obtiene la **interfaz IWMCodecAMVideoAccelerator** del método **IWMReaderAccelerator::GetCodecInterface del** lector. Si el códec no admite DirectX VA, la llamada a **GetCodecInterface** puede producir un error. En este caso, la negociación continúa como de costumbre, sin compatibilidad con DirectX VA.
2.  El filtro de origen pasa el **puntero IAMVideoAccelerator** desde el pin pasado a **Conectar** al descodificador DMO a través de **IWMCodecAMVideoAccelerator::SetAcceleratorInterface**.
3.  A continuación, el filtro de origen delega el resto de la operación **IPin::Conectar** al método **CBaseOutputPin::Conectar.** La enumeración de formato con el SDK continúa como lo hace actualmente. Si el códec admite DirectX VA para el contenido que se está conectando, el códec DMO primero presenta esos subtipos va de DirectX, antes de los tipos YUV y RGB admitidos. Si la compatibilidad con DirectX VA está disponible, se intentan los pasos del 7 al 11 en el contexto de un subtipo va de DirectX. El siguiente fragmento de código muestra cómo identificar un subtipo multimedia de DirectX VA.
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  La **implementación de CBaseOutputPin::Conectar** llama a **IPin::CompleteConnect durante** el paso 3. Si se tiene en cuenta un subtipo de VA de DirectX, se intenta la negociación de Va de DirectX. El pin de salida llama **a IWMCodecAMVideoAccelerator::NegotiateConnection** y le pasa el tipo de medio de salida actual.
5.  El descodificador DMO realiza la negociación necesaria con el VMR a través de la **interfaz IAMVideoAccelerator** y devuelve el GUID del subtipo de vídeo que ambos han acordado. El pin de salida delega todas las llamadas **IAMVideoAcceleratorNotify** recibidas durante este proceso a la interfaz **IAMVideoAcceleratorNotify** del descodificador de DMO, que también se puede obtener a través del método **IWMReaderAccelerator::GetCodecInterface.**
6.  Si **NegotiateConnection se** realiza correctamente, el pin de salida llama a **IWMCodecAMVideoAccelerator::SetPlayerNotify** con una **interfaz IWMPlayerTimestampHook.** Este enlace permite que el filtro de origen actualice las marcas de tiempo en los ejemplos antes de que se entreguen al representador.
7.  El filtro de origen llama **a IWMReaderAccelerator::Notify** con el tipo de medio negociado. Esto permite al lector actualizar sus variables internas y confirmar en DirectX VA. Este es el último lugar en el que se puede producir un error en el códec o lector. Si se producirá un error en cualquiera de los pasos anteriores, el filtro de origen debe volver al paso 3 e intentar el siguiente tipo enumerado por el lector.
8.  Se inicia la reproducción. El lector omite los búferes de salida del descodificador DMO si el tipo de salida de conexión es DirectX VA.
9.  Cuando **se produce IPin::D isconnect,** el filtro de origen llama a **IWMCodecAMVideoAccelerator::SetAcceleratorInterface** con **un valor NULL.** Esto interrumpe la conexión de DirectX VA entre el códec y el representador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




