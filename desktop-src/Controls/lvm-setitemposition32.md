---
title: LVM_SETITEMPOSITION32 mensaje (Commctrl.h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en la vista de icono o icono pequeño).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362687"
---
# <a name="lvm_setitemposition32-message"></a>Mensaje \_ LVM SETITEMPOSITION32

Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en la vista de icono o icono pequeño). Este mensaje difiere del mensaje [**\_ SETITEMPOSITION de LVM**](lvm-setitemposition.md) en que usa coordenadas de 32 bits. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetItemPosition32.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista para el que se va a establecer la posición.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que contiene la nueva posición del elemento, en coordenadas de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

