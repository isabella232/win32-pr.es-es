---
title: LVM_GETSTRINGWIDTH mensaje (Commctrl.h)
description: Determina el ancho de una cadena especificada utilizando la fuente actual del control list-view especificado. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetStringWidth.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019313"
---
# <a name="lvm_getstringwidth-message"></a>Mensaje \_ GETSTRINGWIDTH de LVM

Determina el ancho de una cadena especificada utilizando la fuente actual del control list-view especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetStringWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de cadena si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

El mensaje LVM \_ GETSTRINGWIDTH devuelve el ancho exacto, en píxeles, de la cadena especificada. Si usa el ancho de cadena devuelto como ancho de columna en el mensaje [**LVM \_ SETCOLUMNWIDTH,**](lvm-setcolumnwidth.md) la cadena se truncará. Para recuperar el ancho de columna que puede contener la cadena sin truncarla, debe agregar relleno al ancho de cadena devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) y **LVM \_ GETSTRINGWIDLG** (ANSI)<br/>     |



 

 





