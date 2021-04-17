---
title: Habilitar la aceleración de vídeo de DirectX
description: Habilitar la aceleración de vídeo de DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- SDK de Windows Media Format, habilitar DXVA
- Windows Media Format SDK, DirectX video Acceleration (DXVA)
- SDK de Windows Media Format, aceleración de vídeo
- Advanced Systems Format (ASF), habilitar DXVA
- ASF (formato de sistemas avanzados), habilitar DXVA
- Advanced Systems Format (ASF), DirectX video Acceleration (DXVA)
- ASF (formato de sistemas avanzados), aceleración de vídeo de DirectX (DXVA)
- Advanced Systems Format (ASF), aceleración de vídeo
- ASF (formato de sistemas avanzados), aceleración de vídeo
- Aceleración de vídeo de DirectX (DXVA), habilitar
- DXVA (aceleración de vídeo de DirectX), habilitar
- Aceleración de vídeo DirectX (DXVA), orden de operaciones
- DXVA (aceleración de vídeo DirectX), orden de operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420239"
---
# <a name="enabling-directx-video-acceleration"></a>Habilitar la aceleración de vídeo de DirectX

En esta sección se describe cómo habilitar la aceleración de vídeo de Microsoft® DirectX® al reproducir contenido transmitido en un reproductor personalizado.

## <a name="background"></a>Información previa

DirectX video Acceleration (DirectX VA) es una especificación de API para la aceleración de hardware de las operaciones de descodificación 2D. Permite a los descodificadores de software descargar ciertas operaciones de uso intensivo de la CPU en la tarjeta gráfica para su procesamiento. En el caso de los usuarios finales, esto hace posible vídeo de alta velocidad, como la reproducción de DVD a pantalla completa, en equipos más antiguos equipados con tarjetas gráficas compatibles con DirectX VA.

A partir del SDK de Windows Media Format 9 series, el filtro de contenedor de DMO es compatible con DirectX VA. Esto significa que, para la reproducción local, las aplicaciones pueden usar el filtro de lector ASF de WM para reproducir contenido basado en Windows Media y la aceleración de hardware de DirectX VA se invocará automáticamente si la tarjeta gráfica lo admite. Sin embargo, el filtro de lector ASF de WM no admite la reproducción de contenido transmitido por secuencias. Por lo tanto, si desea admitir DirectX VA al reproducir contenido transmitido en un reproductor personalizado, debe usar un mecanismo alternativo, que es el que usa Windows Media Player a partir de la serie Windows Media 9.

Dado que Windows Media Player se diseñó antes de que se hubiesen desarrollado los filtros de QASF, Windows Media Player tiene su propio filtro de origen, basado en el SDK de Windows Media Format, para reproducir contenido basado en Windows Media. El filtro de origen de Windows Media de WMP proporciona datos descomprimidos de nivel inferior directamente a los representadores de audio y vídeo. Por el contrario, el lector ASF de WM entrega el contenido comprimido de nivel inferior a los objetos multimedia DirectX de Windows Media descodificador (DMOs), que se hospedan en el contenedor de DMO. En los diagramas siguientes se muestran las diferencias entre el lector ASF de WM y el filtro de origen de Windows Media de WMP.

![el filtro de origen personalizado genera muestras sin comprimir](images/wmp-dxva-graph.png)

![el filtro de origen qasf muestra ejemplos comprimidos](images/qasf-dxva-graph.png)

Para habilitar DirectX VA para el contenido transmitido por secuencias, debe crear un filtro de origen personalizado como el del diagrama superior. Básicamente, este filtro usará el SDK de Windows Media Format para crear una instancia de un objeto de lector de WM, descomprimir los ejemplos y enviarlos en orden descendente en sus clavijas de salida. En este debate se supone que ya ha creado el filtro de origen y ahora está listo para implementar la compatibilidad con DirectX VA.

Para habilitar DirectX VA, la tarea básica del filtro de origen es proporcionar el representador de vídeo y el descodificador WMV DMO con las interfaces que deberán negociar la conexión de DirectX VA. El filtro de origen no participa en esas negociaciones. Una vez que se inicia el streaming, la única tarea relacionada con DirectX VA que puede realizar el filtro de origen es modificar las marcas de tiempo de las muestras de vídeo antes de que el descodificador WMV las entregue al representador de vídeo. La razón principal para hacerlo es proporcionar un control de escala de tiempo personalizado más allá de lo que habilitan las interfaces estándar de DirectShow®.

Se definen tres interfaces para habilitar las comunicaciones necesarias entre el SDK de Windows Media Format, el filtro de origen del reproductor, el Windows Media Video descodificador DMO y el mezclador de superposición o el representador de mezcla de vídeo. Estas interfaces se describen en la tabla siguiente.



| Interfaz                                                        | Descripción                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Expuesto por el descodificador de Windows Media DMO y llamado por el filtro de origen de un reproductor multimedia para configurar las distintas conexiones necesarias para habilitar DirectX VA para la descodificación del contenido de Windows Media Video. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implementado en el filtro de origen del reproductor. Permite que el filtro modifique las marcas de tiempo en las muestras de vídeo antes de entregarlas en orden descendente.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implementado en el objeto lector de WM. Lo llama un filtro de origen del reproductor para obtener interfaces del descodificador DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Orden de operaciones en DirectX: reproducción habilitada

En esta sección se describe el orden general de las operaciones en tiempo de ejecución para un reproductor habilitado para DirectX y su filtro de origen. Los componentes a los que se hace referencia en esta sección son:

-   Un reproductor multimedia de terceros, denominado reproductor.
-   Un filtro de origen personalizado, al que se ha creado una instancia del reproductor, que usa el SDK de Windows Media Format para descomprimir el contenido basado en Windows Media.
-   La clavija de salida de vídeo del filtro de origen del reproductor, que se conoce como el PIN de salida.
-   Gráfico de filtro de reproducción de vídeo de DirectShow, denominado gráfico.
-   El representador de mezcla de vídeo, denominado VMR.
-   Objeto lector asincrónico del SDK de formato de Windows Media, al que se hace referencia como lector.
-   El objeto multimedia de DirectX del descodificador de Windows Media Video, conocido como descodificador DMO.

El orden de las operaciones es el siguiente:

1.  El reproductor crea instancias de su filtro de origen y un objeto de lector. El lector crea un descodificador de vídeo DMO y establece el tipo de entrada (comprimido) en él. Esto debe ocurrir antes de que el reproductor intente configurar el gráfico de reproducción de vídeo porque el SDK y el descodificador DMO deben estar implicados en el proceso de negociación con el gráfico, y el DMO debe conocer el formato de entrada durante el paso 9.
2.  El reproductor llama a **IGraphBuilder:: Render**, proporcionándole el PIN de salida del filtro de origen de vídeo. En este momento, el administrador de gráficos de filtros de DirectShow intenta conectar el VMR al filtro de origen de vídeo del reproductor.
3.  El administrador de gráficos de filtro llama a **IPin:: Connect** en el PIN de salida del filtro de origen de vídeo del reproductor.

Los pasos 4 a 10 se producen dentro de **IPin:: Connect**.

1.  El filtro de origen obtiene la interfaz **IWMCodecAMVideoAccelerator** del método **IWMReaderAccelerator:: GetCodecInterface** del lector. Si el códec no es compatible con DirectX VA, puede producirse un error en la llamada a **GetCodecInterface** . En este caso, la negociación continúa de la forma habitual, sin compatibilidad con DirectX.
2.  El filtro de origen pasa el puntero **IAMVideoAccelerator** del PIN pasado en **Connect** al descodificador DMO a través de **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface**.
3.  A continuación, el filtro de origen delega el resto de la operación **IPin:: Connect** en el método **CBaseOutputPin:: Connect** . La enumeración de formato con el SDK continúa como hace hoy. Si el códec es compatible con DirectX VA para el contenido que se está conectando, el códec DMO presenta los subtipos de DirectX VA en primer lugar, antes de que se admitan los tipos YUV y RGB. Si está disponible la compatibilidad con DirectX VA, se intentan los pasos 7 a 11 en el contexto de un subtipo de DirectX VA. En el fragmento de código siguiente se muestra cómo identificar un subtipo de medios de DirectX VA.
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

    

4.  La implementación de **CBaseOutputPin:: Connect** llama a **IPin:: CompleteConnect** durante el paso 3. Si se está considerando un subtipo de DirectX VA, se intenta la negociación de DirectX VA. El PIN de salida llama a **IWMCodecAMVideoAccelerator:: NegotiateConnection**, pasándole el tipo de medio de salida actual.
5.  El descodificador DMO realiza la negociación necesaria con la VMR a través de la interfaz **IAMVideoAccelerator** y devuelve el GUID del subtipo de vídeo que han acordado los dos. El PIN de salida delega todas las llamadas de **IAMVideoAcceleratorNotify** recibidas durante este proceso a la interfaz **IAMVideoAcceleratorNotify** del descodificador DMO, que también se puede obtener a través del método **IWMReaderAccelerator:: GetCodecInterface** .
6.  Si **NegotiateConnection** se ejecuta correctamente, el PIN de salida llama a **IWMCodecAMVideoAccelerator:: SetPlayerNotify** con una interfaz **IWMPlayerTimestampHook** . Este enlace permite que el filtro de origen actualice las marcas de tiempo de los ejemplos antes de que se entreguen al representador.
7.  El filtro de origen llama a **IWMReaderAccelerator:: Notify** con el tipo de medio negociado. Esto permite al lector actualizar sus variables internas y confirmar a DirectX VA. Este es el último lugar en el que se puede producir un error en el lector o el lector. Si se produce un error en cualquiera de los pasos anteriores, el filtro de origen debe volver al paso 3 y probar el siguiente tipo enumerado por el lector.
8.  Se inicia la reproducción. El lector omite los búferes de salida del descodificador DMO si el tipo de salida de la conexión es DirectX.
9.  Cuando se produce **IPin::D Ulta** , el filtro de origen llama a **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface** con un **valor null**. Esto interrumpe la conexión de DirectX VA entre el códec y el representador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




