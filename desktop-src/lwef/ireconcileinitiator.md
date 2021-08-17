---
title: Interfaz IReconcileInitiator
description: Expone métodos que proporcionan al conciliador de mal estado los medios para notificar al iniciador su progreso, para establecer un objeto de terminación y para solicitar una versión determinada de un documento. El iniciador es responsable de implementar esta interfaz.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- IReconcileInitiator interface Legacy Windows Environment Features
- Interfaz IReconcileInitiator Características heredadas del entorno Windows , descritas
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
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749145"
---
# <a name="ireconcileinitiator-interface"></a>Interfaz IReconcileInitiator

Expone métodos que proporcionan al conciliador de mal estado los medios para notificar al iniciador su progreso, para establecer un objeto de terminación y para solicitar una versión determinada de un documento. El iniciador es responsable de implementar esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IReconcileInitiator** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IReconcileInitiator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IReconcileInitiator tiene** estos métodos.



| Método                                                                 | Descripción                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Establece el objeto a través del cual el iniciador puede finalizar de forma asincrónica una conciliación. Normalmente, un conciliador de minúsculas establece este objeto para las conciliaciones que son largas o implican la interacción del usuario. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indica la cantidad de progreso que ha realizado el conciliador de mal estado para completar la conciliación. La cantidad es una fracción y se calcula como cociente de los parámetros *ulProgress* y *ulProgressMax.* Los reconciliadores deben llamar a este método periódicamente durante su proceso de conciliación. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.0 o posterior)</dt> </dl> |



 

