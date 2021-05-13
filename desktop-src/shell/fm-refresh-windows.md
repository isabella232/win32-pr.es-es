---
description: Enviado por una extensión del Administrador de archivos para hacer que el Administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.
title: FM_REFRESH_WINDOWS mensaje (Wfext.h)
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
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842356"
---
# <a name="fm_refresh_windows-message"></a>Mensaje \_ DE WINDOWS DE ACTUALIZACIÓN DE \_ FM

Enviado por una extensión del Administrador de archivos para hacer que el Administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*fRepaint* 
</dt> <dd>

Valor que indica si el Administrador de archivos vuelve a dibujar su ventana activa o todas sus ventanas. Si este parámetro es **TRUE,** el Administrador de archivos vuelve a dibujar todas sus ventanas. De lo contrario, el Administrador de archivos vuelve a dibujar solo su ventana activa.

</dd> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El Administrador de archivos detecta automáticamente los cambios del sistema de archivos causados por una extensión. Una extensión debe usar este mensaje solo en situaciones en las que se realizan o cancelan conexiones de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




