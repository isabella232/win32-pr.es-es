---
title: Mensaje de PGM_SETBORDER (commctrl. h)
description: Establece el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetBorder de buscapersonas \_ .
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079268"
---
# <a name="pgm_setborder-message"></a>\_Mensaje SETBORDER PGM

Establece el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBorder de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo tamaño del borde, en píxeles. Este valor no debe ser mayor que el botón de buscapersonas o menor que cero. Si *lParam* es demasiado grande, el borde se dibujará con el mismo tamaño que el botón. Si *lParam* es negativo, el tamaño del borde se establecerá en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene el tamaño de borde anterior, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





