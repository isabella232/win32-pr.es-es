---
title: Acerca de IMediaObject
description: Acerca de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IMediaObject
- complementos, interfaz IMediaObject
- Complementos de procesamiento de señal digital, interfaz IMediaObject
- Complementos DSP, interfaz IMediaObject
- Interfaz IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773584"
---
# <a name="about-imediaobject"></a>Acerca de IMediaObject

La interfaz **IMediaObject** es la interfaz necesaria para DMOs. **IMediaObject** contiene los métodos que usa un complemento DSP de Windows Media Player para obtener datos de Windows Media Player, para procesar los datos y para devolver los datos procesados a Media Player de Windows. Para obtener la documentación completa de la interfaz **IMediaObject** , consulte la sección DirectShow de la Windows SDK.

Los métodos de **IMediaObject** se pueden categorizar de la manera siguiente:

## <a name="methods-that-handle-format-negotiation"></a>Métodos que controlan la negociación de formato

Estos son los métodos que Windows Media Player llama para obtener información sobre los formatos de datos admitidos por el complemento. Esos métodos incluyen:

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **SetOutputType**

Algunos de estos métodos, como **GetInputType** y **SetInputType**, usan la estructura **de \_ \_ tipo de medio DMO** para describir el formato de los datos usados por un flujo. Cuando Windows Media Player llama a estos métodos, proporciona un puntero a una estructura de **\_ \_ tipo de medio DMO** . Si un método como **SetInputType** especifica la información de tipo de medio, el complemento debe copiar la estructura **de \_ \_ tipo de medio DMO** en una variable miembro e inspeccionar sus miembros de datos para determinar el tipo de datos que Windows Media Player proporcionará en el búfer de entrada. Si un método como **GetInputType** recupera la información de tipo de archivo multimedia, el complemento debe copiar la dirección de la variable miembro que contiene la estructura de **\_ \_ tipo de medio DMO** en el puntero proporcionado por Media Player de Windows en la lista de parámetros.

Windows Media Player usa principalmente dos miembros de la estructura de **\_ \_ tipo de medio DMO** :

-   **majortype**: un identificador único global (GUID) que especifica la categoría general del medio, como audio o vídeo.
-   **SubType**: un GUID que especifica una descripción más detallada del medio, como audio PCM.

Estos GUID se pueden encontrar en el encabezado denominado UUID. h, que se incluye con el Windows SDK.

Los métodos como **GetInputSizeInfo** proporcionan información a Windows Media Player sobre cuánta memoria se necesita para asignar los búferes de procesamiento. Los métodos como **GetStreamCount** y **GetOutputStreamInfo** proporcionan información a Windows Media Player sobre el número y el carácter de las secuencias admitidas por el complemento DSP.

**GetInputMaxLatency** y **SetInputMaxLatency** se implementan mediante DMOs en casos especiales. Los complementos DSP de Windows Media Player deben devolver E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especifican o recuperan información de estado

Estos son los métodos que Windows Media Player llama para obtener o establecer valores relacionados con el estado actual del complemento. Esos métodos incluyen:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** y **GetOutputCurrentType** usan la estructura de **\_ \_ tipo de medio DMO** para devolver información a Windows Media Player acerca de los tipos de medios previamente establecidos para los flujos de entrada y salida. **GetInputStatus** devuelve una marca que indica a Windows Media Player si el complemento DSP puede aceptar datos de entrada.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que controlan los datos de procesamiento y almacenamiento en búfer

Estos son los métodos que Windows Media Player llama para iniciar los distintos procesos que el complemento realiza para realizar el procesamiento de la señal digital. Esos métodos incluyen:

-   **AllocateStreamingResources**
-   **Discontinuidad**
-   **Vaciar**
-   **FreeStreamingResources**
-   **Bloquear**
-   **ProcessInput**
-   **ProcessOutput**

Windows Media Player llama a **AllocateStreamingResources** y **FreeStreamingResources** para proporcionar al complemento DSP la oportunidad de configurar o liberar los búferes adicionales que el complemento pueda necesitar para el procesamiento interno.

Los complementos DSP de Windows Media Player no necesitan usar el método de **discontinuidad** de DMO.

Windows Media Player llama a **Flush** para dirigir el complemento DSP para vaciar todos los datos almacenados en el búfer interno. El complemento debe liberar todas las referencias a las interfaces de **IMediaBuffer** , borrar cualquier valor que especifique la marca de tiempo o la longitud de muestra para el búfer multimedia, y reinicializar los Estados internos que dependen del contenido del ejemplo multimedia.

Windows Media Player llama a ProcessInput para pasar un puntero a una interfaz **IMediaBuffer** al complemento DSP. Esta interfaz proporciona acceso al búfer de entrada asignado por Windows Media Player para proporcionar datos al complemento. Windows Media Player llama posteriormente a **ProcessOutput** para pasar un puntero a una interfaz **IMediaBuffer** que proporciona acceso al búfer de salida asignado por Windows Media Player para recibir los datos procesados del complemento DSP.

La interfaz **IMediaObject** incluye un método denominado **Lock**. Este método está diseñado para adquirir o liberar un bloqueo en DMO con el fin de mantener la serialización de DMO al realizar varias operaciones. La versión de **IMediaObject:: Lock** en el código del asistente invalida la implementación ATL de **Lock**. Dado que Windows Media Player serializa las llamadas realizadas a la interfaz DMO de un complemento DSP, la implementación de **Lock** simplemente devuelve S \_ OK. Para obtener más información sobre cómo crear un DMO multiproceso, consulte la sección de DirectShow del Windows SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




