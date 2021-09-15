---
title: MPCLEAN_PRECHECK_DATA estructura (MpClient.h)
description: Datos de notificación pasados para limpiar la función de devolución de llamada de comprobación previa.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA estructura heredada de Windows environment
- PMPCLEAN_PRECHECK_DATA puntero de estructura heredados Windows environment features
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
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248624"
---
# <a name="mpclean_precheck_data-structure"></a>ESTRUCTURA \_ DE DATOS DE PRECHECK DE MPCLEAN \_

Datos de notificación pasados para limpiar la función de devolución de llamada de comprobación previa.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Información de recursos sobre el recurso que se está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**PMPRESOURCE \_ INFO**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Información de recursos sobre el recurso que está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Vea [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> </dl>

 

 





