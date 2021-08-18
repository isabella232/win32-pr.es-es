---
title: MPCLEAN_PRECHECK_DATA estructura (MpClient.h)
description: Datos de notificación pasados para limpiar la función de devolución de llamada de comprobación previa.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA estructura heredada de Windows environment
- PMPCLEAN_PRECHECK_DATA puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747931"
---
# <a name="mpclean_precheck_data-structure"></a>Estructura \_ DE DATOS DE PRECHECK de MPCLEAN \_

Datos de notificación pasados para limpiar la función de devolución de llamada de comprobación previa.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Información de recursos sobre el recurso que se está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Consulte [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**PMPRESOURCE \_ INFO**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Información de recursos sobre el recurso que está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Consulte [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> </dl>

 

 





