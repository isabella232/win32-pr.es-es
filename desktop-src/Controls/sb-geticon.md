---
title: Mensaje de SB_GETICON (commctrl. h)
description: Recupera el icono de un elemento en una barra de estado.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905459"
---
# <a name="sb_geticon-message"></a>\_Mensaje GETICON de SB

Recupera el icono de un elemento en una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que contiene el icono que se va a recuperar. Si este parámetro es-1, se supone que la barra de estado es una barra de estado de [modo simple](status-bars.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del icono si se realiza correctamente o **null** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





