---
title: Código de notificación de EN_CLIPFORMAT (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha realizado una copia con un formato de Portapapeles determinado. Un control Rich Edit sin ventanas envía esta notificación mediante el método ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT controles de código de notificación de Windows
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
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996218"
---
# <a name="en_clipformat-notification-code"></a>\_Código de notificación en CLIPFORMAT

Notifica a la ventana primaria de un control Rich Edit que se ha realizado una copia con un formato de Portapapeles determinado. Un control Rich Edit sin ventanas envía esta notificación mediante el método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

IDENTIFICADOR de ventana que se ha recuperado mediante una llamada a la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contiene información sobre el formato del portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para recibir los \_ códigos de notificación en CLIPFORMAT, especifique [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

