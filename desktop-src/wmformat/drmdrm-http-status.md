---
title: Enumeración DRM_HTTP_STATUS (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración de estado http de DRM define un intervalo de Estados http para una solicitud DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709142"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>Enumeración DRM_HTTP_STATUS (wmdrmsdk. h)

El tipo de enumeración de **\_ \_ Estado http de DRM** define un intervalo de Estados http para una solicitud DRM.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**
</dt> <dd>

No se han iniciado las operaciones HTTP.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_Conexión http**
</dt> <dd>

Se está estableciendo la conexión.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitud http**
</dt> <dd>

Se están solicitando los datos.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_recepción http**
</dt> <dd>

Se están recibiendo los datos.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completado**
</dt> <dd>

Las operaciones HTTP se han completado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la estructura de [**\_ \_ Estado**](drmwm-individualize-status.md) de la función de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





