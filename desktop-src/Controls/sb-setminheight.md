---
title: SB_SETMINHEIGHT mensaje (Commctrl.h)
description: Establece el alto mínimo del área de dibujo de una ventana de estado.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT controles de Windows mensaje
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
ms.openlocfilehash: 1b644067e48312b265d132f7d06d53343c4612b879c3a09b638ebd0a98a7c88a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293735"
---
# <a name="sb_setminheight-message"></a>Mensaje \_ SB SETMINHEIGHT

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

## <a name="remarks"></a>Comentarios

El alto mínimo es la suma de *wParam* y el doble del ancho, en píxeles, del borde vertical de la ventana de estado. Una aplicación debe enviar el [**mensaje WM \_ SIZE**](/windows/desktop/winmsg/wm-size) a la ventana de estado para volver a dibujar la ventana. Los *parámetros wParam* *y lParam* del mensaje WM **\_ SIZE** deben establecerse en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

