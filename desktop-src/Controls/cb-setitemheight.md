---
title: CB_SETITEMHEIGHT mensaje (Winuser.h)
description: Una aplicación envía un mensaje CB SETITEMHEIGHT para establecer el alto de los elementos de lista o el \_ campo de selección en un cuadro combinado.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170110"
---
# <a name="cb_setitemheight-message"></a>Mensaje \_ DE CB SETITEMHEIGHT

Una aplicación envía un mensaje **\_ CB SETITEMHEIGHT** para establecer el alto de los elementos de lista o el campo de selección en un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el componente del cuadro combinado para el que se va a establecer el alto.

Este parámetro debe ser 1 para establecer el alto del campo de selección. Debe ser cero para establecer el alto de los elementos de lista, a menos que el cuadro combinado tenga el estilo [**\_ CBS OWNERDRAWVARIABLE.**](combo-box-styles.md) En ese caso, el *parámetro wParam* es el índice de base cero de un elemento de lista específico.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el alto, en píxeles, del componente de cuadro combinado identificado *por wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el índice o alto no es válido, el valor devuelto es CB \_ ERR.

## <a name="remarks"></a>Observaciones

El alto del campo de selección en un cuadro combinado se establece independientemente del alto de los elementos de lista. Una aplicación debe asegurarse de que el alto del campo de selección no sea menor que el alto de un elemento de lista determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





