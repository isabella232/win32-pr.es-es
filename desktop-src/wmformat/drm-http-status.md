---
title: Enumeración DRM_HTTP_STATUS (Drmexternals. h)
description: El \_ \_ tipo de enumeración de estado http de DRM define un intervalo de Estados para una solicitud DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676865"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>Enumeración DRM_HTTP_STATUS (Drmexternals. h)

El tipo de enumeración de **\_ \_ Estado http de DRM** define un intervalo de Estados para una solicitud [*DRM*](wmformat-glossary.md) .

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

Esta enumeración se usa en la estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Estado de individualización de DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





