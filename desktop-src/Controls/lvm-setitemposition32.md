---
title: Mensaje de LVM_SETITEMPOSITION32 (commctrl. h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079430"
---
# <a name="lvm_setitemposition32-message"></a>\_Mensaje SETITEMPOSITION32 LVM

Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños). Este mensaje difiere del mensaje [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) en que usa coordenadas de 32 bits. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemPosition32 de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista para el que se va a establecer la posición.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene la nueva posición del elemento, en coordenadas de la vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

