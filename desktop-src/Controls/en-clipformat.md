---
title: EN_CLIPFORMAT de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que se produjo una pegar con un formato de Portapapeles determinado. Un control de edición enriquecido sin ventanas envía esta notificación mediante el método TxNotify de ITextHost.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437045"
---
# <a name="en_clipformat-notification-code"></a>Código de notificación DE EN \_ CLIPFORMAT

Notifica a la ventana primaria de un control de edición enriquecido que se produjo una pegar con un formato de Portapapeles determinado. Un control de edición enriquecido sin ventanas envía esta notificación mediante el [**método ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de ventana recuperado mediante una llamada a la [**función GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL. \_

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contiene información sobre el formato del Portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Para recibir los códigos de notificación de \_ EN CLIPFORMAT, especifique [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

