---
title: CB_GETITEMHEIGHT mensaje (Winuser.h)
description: Determina el alto de los elementos de lista o el campo de selección en un cuadro combinado.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062536"
---
# <a name="cb_getitemheight-message"></a>Mensaje \_ GETITEMHEIGHT de CB

Determina el alto de los elementos de lista o el campo de selección en un cuadro combinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Componente de cuadro combinado cuyo alto se va a recuperar. Este parámetro debe ser -1 para recuperar el alto del campo de selección. Debe ser cero para recuperar el alto de los elementos de lista, a menos que el cuadro combinado tenga el estilo [**\_ CBS OWNERDRAWVARIABLE.**](combo-box-styles.md) En ese caso, el *parámetro wParam* es el índice de base cero de un elemento de lista específico.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el alto, en píxeles, de los elementos de lista de un cuadro combinado. Si el cuadro combinado tiene el estilo [**CBS \_ OWNERDRAWVARIABLE,**](combo-box-styles.md) es el alto del elemento especificado por el *parámetro wParam.* Si *wParam es* -1, el valor devuelto es el alto de la parte del control de edición (o texto estático) del cuadro combinado. Si se produce un error, el valor devuelto es CB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





