---
title: Código de notificación de EN_CORRECTTEXT (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que \_ se ha producido un gesto SyV correcto, lo que permite a la ventana primaria tener la posibilidad de cancelar la corrección del texto. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149944"
---
# <a name="en_correcttext-notification-code"></a>\_Código de notificación en CORRECTTEXT

Notifica a una ventana primaria de un control Rich Edit que \_ se ha producido un gesto SyV correcto, lo que permite a la ventana primaria tener la posibilidad de cancelar la corrección del texto. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica la selección que se va a corregir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para omitir la acción.

Devuelve un valor distinto de cero para procesar la acción.

## <a name="remarks"></a>Observaciones

Este código de notificación se envía solo si están disponibles las capacidades del lápiz.

Para recibir los \_ códigos de notificación en CORRECTTEXT, especifique [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> El \_ código de notificación en CORRECTTEXT solo se admite en la versión de edición enriquecida 1,0. No se admite en versiones posteriores de Rich Edit. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





