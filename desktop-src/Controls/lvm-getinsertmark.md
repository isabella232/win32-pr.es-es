---
title: LVM_GETINSERTMARK mensaje (Commctrl.h)
description: Recupera la posición del punto de inserción.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061835"
---
# <a name="lvm_getinsertmark-message"></a>Mensaje \_ GETINSERTMARK de LVM

Recupera la posición del punto de inserción.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estructura LVINSERTMARK</a> que recibe la posición del punto de inserción.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario. **Se** devuelve FALSE si el tamaño del **miembro cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura.

## <a name="remarks"></a>Observaciones

Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, la vista de icono pequeño o la vista de mosaico, y no está en modo de vista de grupo.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





