---
title: Código de notificación de EN_DROPFILES (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario está intentando colocar archivos en el control. Un control Rich Edit envía este código de notificación en forma de mensaje de notificación de WM \_ cuando recibe el mensaje de DROPFILES de WM \_ .
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489286"
---
# <a name="en_dropfiles-notification-code"></a>\_Código de notificación en DROPFILES

Notifica a una ventana primaria de un control Rich Edit que el usuario está intentando colocar archivos en el control. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) cuando recibe el mensaje de [**\_ DROPFILES de WM**](/windows/desktop/shell/wm-dropfiles) .


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recibe la información de los archivos colocados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para permitir la operación de colocar.

Devuelve cero para omitir la operación de colocar.

## <a name="remarks"></a>Observaciones

Para que un control de edición enriquecido reciba mensajes de [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) , la ventana primaria debe registrar el control como destino de colocación mediante la función [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) . El control no se registra a sí mismo.

Para recibir los \_ códigos de notificación en DROPFILES, especifique [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

