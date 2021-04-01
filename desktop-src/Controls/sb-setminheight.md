---
title: Mensaje de SB_SETMINHEIGHT (commctrl. h)
description: Establece el alto mínimo del área de dibujo de una ventana de estado.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996809"
---
# <a name="sb_setminheight-message"></a>\_Mensaje SETMINHEIGHT de SB

Establece el alto mínimo del área de dibujo de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Alto mínimo, en píxeles, de la ventana.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El alto mínimo es la suma de *wParam* y el doble de ancho, en píxeles, del borde vertical de la ventana de estado. Una aplicación debe enviar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) a la ventana de estado para volver a dibujar la ventana. Los parámetros *wParam* e *lParam* del mensaje **de \_ tamaño de WM** deben establecerse en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

