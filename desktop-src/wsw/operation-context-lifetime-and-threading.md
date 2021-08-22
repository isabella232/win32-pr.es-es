---
title: Duración del contexto de operación y subprocesamiento
description: La duración del contexto de la operación, representada por un identificador WS OPERATION CONTEXT, determina la duración \_ de las propiedades que \_ contiene.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Duración del contexto de operación y servicios web de subprocesos para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd2748f797e43bab750f4e02409e62e6293b39cb44d4cfd3626f86099502fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344835"
---
# <a name="operation-context-lifetime-and-threading"></a>Duración del contexto de operación y subprocesamiento

La duración del contexto de la operación, representada por un [identificador \_ WS OPERATION \_ CONTEXT,](ws-operation-context.md) determina la duración de las propiedades que contiene. Por lo tanto, solo se debe usar un contexto durante la vigencia de la operación [de servicio](service-operation.md) o la devolución de llamada a la que se proporciona. La duración de una llamada sincrónica es la ejecución de la propia función. Para una llamada asincrónica, la duración finaliza una vez completada la llamada asincrónica. El modelo de servicio no ofrece ninguna garantía sobre el contexto una vez completada la llamada. El comportamiento de confiar en el contexto de la operación o en cualquiera de sus propiedades más allá de su duración no está definido.


Vea también el ejemplo de calculadora basada en sesión [SessionfullCalculatorServiceExample.](sessionfullcalculatorserviceexample.md)

## <a name="threading-model"></a>Modelo de subprocesos

El contexto de la operación admite el subprocesamiento libre, pero esto sucede con el propio contexto de la operación y no se aplica a ninguna de las propiedades que contiene.

Al registrar una devolución de llamada de cancelación para una operación de servicio a través de la función [**WsRegisterOperationForCancel,**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) tenga en cuenta que el primer registro se realizará correctamente. Sin embargo, se producirá un error al establecer la devolución de llamada de cancelación varias veces.

 

 




