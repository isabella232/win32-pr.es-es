---
title: Interfaz IBackgroundCopyManager (Deliveryoptimization.h)
description: Crea trabajos de transferencia, recupera un objeto enumerador que contiene los trabajos de la cola y recupera trabajos individuales de la cola.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cf1ca14443823a5448a63c04d19d00957d4064353183d79aa7762f729115301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542157"
---
# <a name="ibackgroundcopymanager-interface"></a>Interfaz IBackgroundCopyManager

Crea trabajos de transferencia, recupera un objeto enumerador que contiene los trabajos de la cola y recupera trabajos individuales de la cola.

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyManager** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyManager también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyManager** tiene estos métodos.



| Método                                                | Descripción                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Crea un trabajo de transferencia.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Recupera un trabajo especificado de la cola.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

