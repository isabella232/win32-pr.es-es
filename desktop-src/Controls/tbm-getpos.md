---
title: Mensaje de TBM_GETPOS (commctrl. h)
description: Recupera la posición lógica actual del control deslizante en una barra de desplazamiento. Las posiciones lógicas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490697"
---
# <a name="tbm_getpos-message"></a>TBM \_ GETPOS

Recupera la posición lógica actual del control deslizante en una barra de desplazamiento. Las posiciones lógicas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica la posición lógica actual del control deslizante de la barra de desplazamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





