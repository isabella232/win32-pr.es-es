---
title: DRM_HTTP_STATUS enumeración (Wmdrmsdk.h)
description: El tipo de \_ enumeración DRM HTTP \_ STATUS define un intervalo de estados HTTP para una solicitud DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS enumeración windows Media Format
- enumeración windows Media Format
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467085"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>DRM_HTTP_STATUS enumeración (Wmdrmsdk.h)

El **tipo de \_ \_ enumeración DRM HTTP STATUS** define un intervalo de estados HTTP para una solicitud DRM.

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

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**
</dt> <dd>

Las operaciones HTTP no se han iniciado.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**CONEXIÓN \_ HTTP**
</dt> <dd>

Se establece la conexión.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**SOLICITUD \_ HTTP**
</dt> <dd>

Se solicitan datos.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**RECEPCIÓN \_ HTTP**
</dt> <dd>

Se reciben datos.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ COMPLETADO**
</dt> <dd>

Las operaciones HTTP se han completado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura WM [**\_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) utiliza esta enumeración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





