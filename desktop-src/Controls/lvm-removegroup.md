---
title: LVM_REMOVEGROUP mensaje (Commctrl.h)
description: Quita un grupo de un control de vista de lista.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c644a0367747ad63eb15a2b83a8df3078c1c89ca1c51875b178aa22d054de2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062325"
---
# <a name="lvm_removegroup-message"></a>Mensaje \_ REMOVEGROUP de LVM

Quita un grupo de un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador que especifica el grupo que se quitará.</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del grupo si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





