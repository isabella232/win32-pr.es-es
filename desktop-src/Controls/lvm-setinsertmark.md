---
title: LVM_SETINSERTMARK mensaje (Commctrl.h)
description: Establece el punto de inserción en la posición definida.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362706"
---
# <a name="lvm_setinsertmark-message"></a>Mensaje \_ LVM SETINSERTMARK

Establece el punto de inserción en la posición definida.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estructura LVINSERTMARK</a> que especifica dónde establecer el punto de inserción.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario. **Se** devuelve FALSE si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura o cuando no se aplica un punto de inserción en la vista actual.

## <a name="remarks"></a>Observaciones

Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, la vista de icono pequeña o la vista de mosaico, y no está en modo de vista de grupo.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





