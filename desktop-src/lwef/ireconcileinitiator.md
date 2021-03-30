---
title: Interfaz IReconcileInitiator
description: Expone métodos que proporcionan el reconciliador del maletín con los medios para notificar al iniciador de su progreso, establecer un objeto de terminación y solicitar una versión determinada de un documento. El iniciador es responsable de la implementación de esta interfaz.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Interfaz IReconcileInitiator características del entorno heredado de Windows
- Interfaz IReconcileInitiator características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802348"
---
# <a name="ireconcileinitiator-interface"></a>Interfaz IReconcileInitiator

Expone métodos que proporcionan el reconciliador del maletín con los medios para notificar al iniciador de su progreso, establecer un objeto de terminación y solicitar una versión determinada de un documento. El iniciador es responsable de la implementación de esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IReconcileInitiator** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReconcileInitiator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IReconcileInitiator** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Establece el objeto a través del cual el iniciador puede finalizar de forma asincrónica una conciliación. Un reconciliador de maletín normalmente establece este objeto para las reconciliaciones que son largas o que implican la interacción del usuario. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica la cantidad de progreso que ha realizado el reconciliador del maletín para completar la conciliación. La cantidad es una fracción y se calcula como el cociente de los parámetros *ulProgress* y *ulProgressMax* . Los reconciliadores deben llamar a este método periódicamente durante su proceso de conciliación. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,0 o posterior)</dt> </dl> |



 

