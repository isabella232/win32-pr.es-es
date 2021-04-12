---
title: Mensaje de LVM_GETHOTITEM (commctrl. h)
description: Recupera el índice del elemento activo. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHotItem de ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150897"
---
# <a name="lvm_gethotitem-message"></a>\_Mensaje GETHOTITEM LVM

Recupera el índice del elemento activo. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHotItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento que está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





