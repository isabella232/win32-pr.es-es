---
title: SB_GETICON mensaje (Commctrl.h)
description: Recupera el icono de un elemento de una barra de estado.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167161"
---
# <a name="sb_geticon-message"></a>Mensaje \_ SB GETICON

Recupera el icono de un elemento de una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que contiene el icono que se va a recuperar. Si este parámetro es -1, se supone que la barra de estado es una [barra de estado modo](status-bars.md) simple.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al icono si se realiza correctamente o NULL en **caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





