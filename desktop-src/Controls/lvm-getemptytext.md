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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061853"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





