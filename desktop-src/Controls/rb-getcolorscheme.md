---
title: Mensaje de RB_GETCOLORSCHEME (commctrl. h)
description: Recupera la información de la combinación de colores del control rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534665"
---
# <a name="rb_getcolorscheme-message"></a>Mensaje de GETCOLORSCHEME de RB \_

Recupera la información de la combinación de colores del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que recibirá la información de la combinación de colores. Debe establecer el miembro **dwSize** de esta estructura en **sizeof**(COLORSCHEME) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETCOLORSCHEME RB**](rb-setcolorscheme.md)
</dt> </dl>

 

 





