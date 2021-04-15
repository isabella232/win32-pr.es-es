---
title: Acerca de IMFTransform
description: Acerca de IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IMFTransform
- complementos, interfaz IMFTransform
- Complementos de procesamiento de señal digital, interfaz IMFTransform
- Complementos DSP, interfaz IMFTransform
- Interfaz IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695238"
---
# <a name="about-imftransform"></a>Acerca de IMFTransform

La interfaz **IMFTransform** es una de las interfaces que debe implementar un complemento DSP de modo dual. Windows Media Player llama a los métodos de la interfaz **IMFTransform** para proporcionar datos al complemento y recuperar los datos procesados del complemento. Para obtener la documentación completa de la interfaz **IMFTransform** , consulte la sección Media Foundation del Windows SDK.

Los métodos de **IMFTransform** se pueden categorizar de la manera siguiente.

## <a name="methods-that-handle-format-negotiation"></a>Métodos que controlan la negociación de formato

Windows Media Player llama a los métodos siguientes para obtener información sobre los formatos de datos admitidos por el complemento.

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

Windows Media Player llama a los métodos siguientes para obtener o establecer los valores relacionados con el estado actual del complemento.

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
> **SetInputType** y **SetOutputType** se usan para la negociación de formato y para especificar y recuperar información de estado.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Métodos que controlan los datos de procesamiento y almacenamiento en búfer

Windows Media Player llama a los métodos siguientes para iniciar los distintos procesos que realiza el complemento para realizar el procesamiento de la señal digital.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces necesarias**](required-interfaces.md)
</dt> </dl>

 

 




