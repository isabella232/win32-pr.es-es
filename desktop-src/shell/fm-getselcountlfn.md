---
description: Enviado por una extensión del administrador de archivos para recuperar el número de archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.
title: Mensaje de FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997745"
---
# <a name="fm_getselcountlfn-message"></a>\_Mensaje GETSELCOUNTLFN de FM

Enviado por una extensión del administrador de archivos para recuperar el número de archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de archivos seleccionados.

## <a name="remarks"></a>Observaciones

Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones basadas en red) deben utilizar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




