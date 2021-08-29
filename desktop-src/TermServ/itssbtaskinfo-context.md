---
title: Propiedad Context de ITsSbTaskInfo
description: Recupera los bytes de contexto asociados a la tarea.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Propiedades de contexto Servicios de Escritorio remoto
- Propiedad context Servicios de Escritorio remoto interfaz , ITsSbTaskInfo
- Interfaz ITsSbTaskInfo Servicios de Escritorio remoto , propiedad Context
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6b733de4bb969e8b8ed65bcc8e080fd49442ba23fbbb16928afafcccb28f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138288"
---
# <a name="itssbtaskinfocontext-property"></a>Propiedad ITsSbTaskInfo::Context

Recupera los bytes de contexto asociados a la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a>Valor de propiedad

Contexto de la tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





