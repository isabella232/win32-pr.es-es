---
title: DRM_HTTP_STATUS enumeración (Drmexternals.h)
description: El tipo de \_ enumeración DRM HTTP \_ STATUS define un intervalo de estados para una solicitud DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS enumeración windows Media Format
- enumeración windows Media Format
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
ms.openlocfilehash: e222cbf24e6333c7105e8564a5ad255693340749aeea32d98bd013bcb40995d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586305"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>DRM_HTTP_STATUS enumeración (Drmexternals.h)

El **tipo de \_ \_ enumeración DRM HTTP STATUS** define un intervalo de estados para una solicitud [*DRM.*](wmformat-glossary.md)

## <a name="syntax"></a>Syntax


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

## <a name="remarks"></a>Comentarios

La estructura WM [**\_ INDIVIDUALIZE \_ STATUS**](wm-individualize-status.md) utiliza esta enumeración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADO \_ DE INDIVIDUALIZACIÓN DE DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





