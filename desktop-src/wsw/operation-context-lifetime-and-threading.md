---
title: Duración del contexto de operación y subprocesamiento
description: La duración del contexto de la operación, representada por un \_ \_ identificador de contexto de operación de WS, determina la duración de las propiedades que contiene.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Duración del contexto de operación y servicios Web de subprocesos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797308"
---
# <a name="operation-context-lifetime-and-threading"></a>Duración del contexto de operación y subprocesamiento

La duración del contexto de la operación, representada por un identificador de [ \_ \_ contexto de operación de WS](ws-operation-context.md) , determina la duración de las propiedades que contiene. Por lo tanto, solo se debe usar un contexto dentro de la duración de la [operación de servicio](service-operation.md) o la devolución de llamada a la que se proporciona. La duración de una llamada sincrónica es la ejecución de la propia función. Para una llamada asincrónica, la duración finaliza una vez completada la llamada asincrónica. El modelo de servicio no proporciona ninguna garantía sobre el contexto una vez completada la llamada. El comportamiento que se basa en el contexto de la operación o en cualquiera de sus propiedades más allá de su duración es indefinido.


Vea también el ejemplo de calculadora basado en sesión, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Modelo de subprocesos

El contexto de la operación admite el subprocesamiento libre, pero esto es cierto en el propio contexto de la operación y no se aplica a ninguna de las propiedades que contiene.

Al registrar una devolución de llamada de cancelación para una operación de servicio a través de la función [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , tenga en cuenta que el primer registro se realizará correctamente. sin embargo, se producirá un error al establecer la devolución de llamada de cancelación varias veces.

 

 




