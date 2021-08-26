---
title: Acerca de IMFTransform
description: Acerca de IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Reproductor de Windows Media complementos,interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
- Reproductor de Windows Media complementos, interfaz DETRANSFORMTransform
- complementos, interfaz DETRANSFORMTransform
- complementos de procesamiento de señales digitales, interfaz DETRANSFORM
- Complementos DSP, interfaz DEFTransform
- Interfaz DETRANSFORMTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903585"
---
# <a name="about-imftransform"></a>Acerca de IMFTransform

La **interfaz IMFTransform** es una de las interfaces que debe implementar un complemento DSP de modo dual. Reproductor de Windows Media llama a los métodos de la interfaz **IMFTransform** para proporcionar datos al complemento y recuperar los datos procesados del complemento. Para obtener documentación completa de **la interfaz DETRANSFORMTRANSFORM,** consulte la Media Foundation sección del SDK de Windows.

Los métodos **de IMFTransform** se pueden clasificar como se muestra a continuación.

## <a name="methods-that-handle-format-negotiation"></a>Métodos que controlan la negociación de formato

Reproductor de Windows Media llama a los métodos siguientes para obtener información sobre los formatos de datos admitidos por el complemento.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **SetOutputType**
-   **GetAttributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Métodos que especifican o recuperan información de estado

Reproductor de Windows Media llama a los métodos siguientes para obtener o establecer valores relacionados con el estado actual del complemento.

-   **SetInputType**
-   **SetOutputType**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType y** **SetOutputType** se usan tanto para la negociación de formato como para especificar y recuperar información de estado.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que controlan el almacenamiento en búfer y el procesamiento de datos

Reproductor de Windows Media llama a los métodos siguientes para iniciar los distintos procesos que realiza el complemento para realizar el procesamiento de señal digital.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




