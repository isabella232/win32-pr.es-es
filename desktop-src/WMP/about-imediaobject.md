---
title: Acerca de IMediaObject
description: Acerca de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Reproductor de Windows Media complementos,interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
- Reproductor de Windows Media complementos,interfaz IMediaObject
- complementos, interfaz IMediaObject
- complementos de procesamiento de señal digital, interfaz IMediaObject
- Complementos DE DSP, interfaz IMediaObject
- Interfaz IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361742"
---
# <a name="about-imediaobject"></a>Acerca de IMediaObject

La **interfaz IMediaObject** es la interfaz necesaria para las DDO. **IMediaObject** contiene los métodos que un complemento DSP de Reproductor de Windows Media usa para obtener datos de Reproductor de Windows Media, procesar los datos y devolver los datos procesados a Reproductor de Windows Media. Para obtener documentación completa de **la interfaz IMediaObject,** consulte la DirectShow del SDK de Windows.

Los métodos **de IMediaObject** se pueden clasificar de la siguiente manera:

## <a name="methods-that-handle-format-negotiation"></a>Métodos que controlan la negociación de formato

Estos son los métodos que Reproductor de Windows Media llamadas para obtener información sobre los formatos de datos admitidos por el complemento. Esos métodos incluyen:

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

Algunos de estos métodos, como **GetInputType** y **SetInputType,** usan la estructura **DMO MEDIA \_ \_ TYPE** para describir el formato de los datos utilizados por una secuencia. Cuando Reproductor de Windows Media estos métodos, proporciona un puntero a un DMO **\_ estructura MEDIA \_ TYPE.** Si un método como **SetInputType** especifica la información del tipo de medio, el complemento debe copiar la estructura **\_ media \_ TYPE** de DMO en una variable miembro e inspeccionar sus miembros de datos para determinar el tipo de datos que Reproductor de Windows Media proporcionará en el búfer de entrada. Si un método como **GetInputType** recupera la información del tipo de medio, el complemento debe copiar la dirección de la variable miembro que contiene la estructura **DMO MEDIA \_ \_ TYPE** en el puntero proporcionado por Reproductor de Windows Media en la lista de parámetros.

Reproductor de Windows Media usa principalmente dos miembros de la **estructura DMO \_ MEDIA \_ TYPE:**

-   **majortype:** identificador único global (GUID) que especifica la categoría general de los medios, como audio o vídeo.
-   **subtipo:** GUID que especifica una descripción más detallada de los medios, como audio PCM.

Estos GUID se pueden encontrar en el encabezado denominado uuids.h, que se incluye con Windows SDK.

Métodos como **GetInputSizeInfo** proporcionan información para Reproductor de Windows Media cantidad de memoria necesaria para asignar los búferes de procesamiento. Métodos como **GetStreamCount** y **GetOutputStreamInfo** proporcionan información para Reproductor de Windows Media sobre el número y el carácter de las secuencias admitidas por el complemento DSP.

Las DDO implementan **GetInputMaxLatency** **y SetInputMaxLatency** en casos especiales. Reproductor de Windows Media Los complementos DE DSP deben devolver E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especifican o recuperan información de estado

Estos son los métodos que Reproductor de Windows Media llamadas para obtener o establecer valores relacionados con el estado actual del complemento. Esos métodos incluyen:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** y **GetOutputCurrentType** usan la estructura **media \_ \_ TYPE** de DMO para devolver información a Reproductor de Windows Media sobre los tipos de medios establecidos previamente para los flujos de entrada y salida. **GetInputStatus devuelve** una marca que indica Reproductor de Windows Media si el complemento DSP puede aceptar datos de entrada.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que controlan el almacenamiento en búfer y el procesamiento de datos

Estos son los métodos que Reproductor de Windows Media llamadas a para iniciar los distintos procesos que realiza el complemento para realizar el procesamiento de señal digital. Esos métodos incluyen:

-   **AllocateStreamingResources**
-   **Discontinuidad**
-   **Vaciar**
-   **FreeStreamingResources**
-   **Bloquear**
-   **ProcessInput**
-   **ProcessOutput**

Reproductor de Windows Media llama a **AllocateStreamingResources** y **FreeStreamingResources** para proporcionar al complemento DSP la oportunidad de configurar o liberar cualquier búfer adicional que el complemento pueda necesitar para el procesamiento interno.

Reproductor de Windows Media Los complementos DE DSP no necesitan usar el método DMO **discontinuidad.**

Reproductor de Windows Media a **Flush para** dirigir el complemento DSP para vaciar todos los datos almacenados internamente en búfer. El complemento debe liberar cualquier referencia a las interfaces **IMediaBuffer,** borrar los valores que especifiquen la marca de tiempo o la longitud de la muestra para el búfer multimedia y reinicializar los estados internos que dependan del contenido del ejemplo multimedia.

Reproductor de Windows Media a ProcessInput para pasar un puntero a una **interfaz IMediaBuffer** al complemento DSP. Esta interfaz proporciona acceso al búfer de entrada asignado por Reproductor de Windows Media para proporcionar datos al complemento. Reproductor de Windows Media posteriormente llama a **ProcessOutput** para pasar un puntero a una interfaz **IMediaBuffer** que proporciona acceso al búfer de salida asignado por Reproductor de Windows Media para recibir los datos procesados del complemento DSP.

La **interfaz IMediaObject** incluye un método denominado **Lock**. Este método está diseñado para adquirir o liberar un bloqueo en el DMO mantener el DMO serializado al realizar varias operaciones. La versión de **IMediaObject::Lock en** el código del asistente invalida la implementación ATL de **Lock**. Dado Reproductor de Windows Media serializa las llamadas realizadas a la interfaz DMO de un complemento DSP, la implementación de **Lock** simplemente devuelve S \_ OK. Para obtener más información sobre cómo crear un DMO multiproceso, consulte la sección DirectShow del SDK Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




