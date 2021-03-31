---
title: Mensaje de LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcula el ancho y el alto aproximados necesarios para mostrar un número determinado de elementos. Puede enviar este mensaje explícitamente o utilizar la \_ macro ApproximateViewRect de ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT controles de mensajes de Windows
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
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995943"
---
# <a name="lvm_approximateviewrect-message"></a>\_Mensaje APPROXIMATEVIEWRECT LVM

Calcula el ancho y el alto aproximados necesarios para mostrar un número determinado de elementos. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ ApproximateViewRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos que se van a mostrar en el control. Si este parámetro se establece en-1, el mensaje utiliza el número total de elementos del control.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la dimensión x propuesta del control, en píxeles. Este parámetro se puede establecer en-1 para permitir que el mensaje use el valor de ancho actual.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es la dimensión y propuesta del control, en píxeles. Este parámetro se puede establecer en-1 para permitir que el mensaje use el valor del alto actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene el ancho aproximado (en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) y el alto (en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necesarios para mostrar los elementos, en píxeles.

## <a name="remarks"></a>Observaciones

Establecer el tamaño del control de vista de lista en función de las dimensiones proporcionadas por este mensaje puede optimizar el redibujo y reducir el parpadeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

