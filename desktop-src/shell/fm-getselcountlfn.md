---
description: Enviado por una extensión del Administrador de archivos para recuperar el número de archivos seleccionados en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.
title: FM_GETSELCOUNTLFN mensaje (Wfext.h)
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
ms.openlocfilehash: ff0884e1b80e4a5a7e6c295bd449c8e1f6d069ced6c988f584108318a98c6891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094180"
---
# <a name="fm_getselcountlfn-message"></a>Mensaje \_ FM GETSELCOUNTLFN

Enviado por una extensión del Administrador de archivos para recuperar el número de archivos seleccionados en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de archivos seleccionados.

## <a name="remarks"></a>Comentarios

Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones compatibles con la red) deben usar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




