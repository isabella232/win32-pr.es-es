---
title: LB_GETITEMHEIGHT mensaje (Winuser.h)
description: Obtiene el alto de los elementos de un cuadro de lista.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c232c172f14774db9dd7c783e18a10f0888190708432b9336208570f0d5031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434335"
---
# <a name="lb_getitemheight-message"></a>Mensaje \_ GETITEMHEIGHT de LB

Obtiene el alto de los elementos de un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento de cuadro de lista. Este índice solo se usa si el cuadro de lista tiene el estilo [**LB \_ OWNERDRAWVARIABLE;**](list-box-styles.md) de lo contrario, debe ser cero.

Windows edición 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el alto, en píxeles, de cada elemento del cuadro de lista. El valor devuelto es el alto del elemento especificado por el parámetro *wParam* si el cuadro de lista tiene el [**estilo LB \_ OWNERDRAWVARIABLE.**](list-box-styles.md) El valor devuelto es \_ LB ERR si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)
</dt> </dl>

 

 





