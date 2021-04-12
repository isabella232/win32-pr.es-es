---
title: MPCLEAN_PRECHECK_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de precomprobación limpia.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCLEAN_PRECHECK_DATA características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490007"
---
# <a name="mpclean_precheck_data-structure"></a>Estructura de datos de \_ comprobación de MPCLEAN \_

Datos de notificación pasados a la función de devolución de llamada de precomprobación limpia.

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

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Información de recursos sobre el recurso que se está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**. Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> <dt>

**información de PMPRESOURCE \_**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Información de recursos sobre el recurso que está bloqueando. Por ejemplo, cuando el progreso es **MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**. Vea [**\_ información de MPRESOURCE**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**información de MPRESOURCE \_**](mpresource-info.md)
</dt> </dl>

 

 





