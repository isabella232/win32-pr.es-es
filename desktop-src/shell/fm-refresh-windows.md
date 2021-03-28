---
description: Enviado por una extensión del administrador de archivos para que el administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.
title: Mensaje de FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275112"
---
# <a name="fm_refresh_windows-message"></a>\_Mensaje de \_ Windows actualizar FM

Enviado por una extensión del administrador de archivos para que el administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*fRepaint* 
</dt> <dd>

Valor que indica si el administrador de archivos vuelve A dibujar su ventana activa o todas sus ventanas. Si este parámetro es **true**, el administrador de archivos vuelve a dibujar todas sus ventanas. De lo contrario, el administrador de archivos vuelve a dibujar solo la ventana activa.

</dd> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El administrador de archivos detecta automáticamente los cambios realizados en el sistema de archivos causados por una extensión. Una extensión solo debe usar este mensaje en situaciones en las que se realizan o cancelan conexiones de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




