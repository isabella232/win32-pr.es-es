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
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224271"
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

## <a name="remarks"></a>Comentarios

El Administrador de archivos detecta automáticamente los cambios del sistema de archivos causados por una extensión. Una extensión debe usar este mensaje solo en situaciones en las que se realizan o cancelan conexiones de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




