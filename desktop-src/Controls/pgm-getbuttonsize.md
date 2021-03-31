---
title: Mensaje de PGM_GETBUTTONSIZE (commctrl. h)
description: Recupera el tamaño actual del botón para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetButtonSize de buscapersonas \_ .
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079561"
---
# <a name="pgm_getbuttonsize-message"></a>\_Mensaje GETBUTTONSIZE PGM

Recupera el tamaño actual del botón para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene el tamaño del botón actual, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETBUTTONSIZE PGM**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





