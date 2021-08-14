---
title: LVM_GETEMPTYTEXT mensaje (Commctrl.h)
description: Obtiene el texto diseñado para mostrarse cuando el control de vista de lista aparece vacío. Envíe este mensaje explícitamente o mediante la macro \_ ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411474"
---
# <a name="lvm_getemptytext-message"></a>Mensaje \_ GETEMPTYTEXT de LVM

Obtiene el texto diseñado para mostrarse cuando el control de vista de lista aparece vacío. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetEmptyText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta *lParam,* incluido el valor **NULL final.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a un búfer Unicode terminado en NULL de tamaño especificado por *wParam* para recibir el texto. El autor de la llamada es responsable de asignar el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





