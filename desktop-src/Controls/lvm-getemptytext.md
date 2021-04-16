---
title: Mensaje de LVM_GETEMPTYTEXT (commctrl. h)
description: Obtiene el texto destinado a mostrarse cuando el control de vista de lista aparece vacío. Envíe este mensaje explícitamente o mediante la \_ macro GetEmptyText de ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489059"
---
# <a name="lvm_getemptytext-message"></a>\_Mensaje GETEMPTYTEXT LVM

Obtiene el texto destinado a mostrarse cuando el control de vista de lista aparece vacío. Envíe este mensaje explícitamente o mediante la [**macro \_ GetEmptyText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta *lParam*, incluido el **valor null** final.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Un puntero a un búfer Unicode de terminación null de tamaño especificado por *wParam* para recibir el texto. El autor de la llamada es responsable de la asignación del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





