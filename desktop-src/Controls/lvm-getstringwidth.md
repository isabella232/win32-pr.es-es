---
title: Mensaje de LVM_GETSTRINGWIDTH (commctrl. h)
description: Determina el ancho de una cadena especificada utilizando la fuente actual del control de vista de lista especificada. Puede enviar este mensaje explícitamente o mediante la \_ macro GetStringWidth de ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH controles de mensajes de Windows
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
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535038"
---
# <a name="lvm_getstringwidth-message"></a>\_Mensaje GETSTRINGWIDTH LVM

Determina el ancho de una cadena especificada utilizando la fuente actual del control de vista de lista especificada. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetStringWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de la cadena si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

El \_ mensaje LVM GETSTRINGWIDTH devuelve el ancho exacto, en píxeles, de la cadena especificada. Si usa el ancho de cadena devuelto como el ancho de columna en el mensaje [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , la cadena se truncará. Para recuperar el ancho de columna que puede contener la cadena sin truncarla, debe agregar relleno al ancho de la cadena devuelta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) y **\_ GETSTRINGWIDTHA de LVM** (ANSI)<br/>     |



 

 





