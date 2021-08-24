---
title: LVM_GETTILEINFO mensaje (Commctrl.h)
description: Recupera información sobre un icono en un control de vista de lista.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8141b3a39c47966348dfd823b557c1b0af4cca84a90ba979a358d6ac0eaa4757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079039"
---
# <a name="lvm_gettileinfo-message"></a>Mensaje \_ GETTILEINFO de LVM

Recupera información sobre un icono en un control de vista de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**estructura LVTILEINFO**</a> que recibe la información recuperada.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor devuelto no utilizado.

## <a name="remarks"></a>Comentarios

La vista de mosaico es una nueva manera de organizar y mostrar elementos en un control de vista de lista. Las demás vistas son icono, icono pequeño, detalles y lista.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





