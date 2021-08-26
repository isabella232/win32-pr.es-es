---
title: LVM_APPROXIMATEVIEWRECT mensaje (Commctrl.h)
description: Calcula el ancho y alto aproximados necesarios para mostrar un número determinado de elementos. Puede enviar este mensaje explícitamente o usar la macro ListView \_ ApproximateViewRect.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047065"
---
# <a name="lvm_approximateviewrect-message"></a>Mensaje \_ DE LVM APPROXIMATEVIEWRECT

Calcula el ancho y alto aproximados necesarios para mostrar un número determinado de elementos. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ ApproximateViewRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se mostrarán en el control . Si este parámetro se establece en -1, el mensaje usa el número total de elementos del control .

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la dimensión X propuesta del control, en píxeles. Este parámetro se puede establecer en -1 para permitir que el mensaje use el valor de ancho actual.

[**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la dimensión y propuesta del control, en píxeles. Este parámetro se puede establecer en -1 para permitir que el mensaje use el valor de alto actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene el ancho aproximado (en [**LOWORD)**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))y el alto (en [**HIWORD)**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))necesarios para mostrar los elementos, en píxeles.

## <a name="remarks"></a>Comentarios

Establecer el tamaño del control de vista de lista en función de las dimensiones proporcionadas por este mensaje puede optimizar el volver a dibujar y reducir el parpadeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

