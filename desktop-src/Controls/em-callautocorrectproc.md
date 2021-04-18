---
title: Mensaje EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Llama a la función de devolución de llamada de Autocorrección almacenada por el \_ mensaje em SETAUTOCORRECTPROC, siempre que el texto que precede al punto de inserción sea un candidato para la corrección automática.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491518"
---
# <a name="em_callautocorrectproc-message"></a>\_Mensaje CALLAUTOCORRECTPROC em

Llama a la función de devolución de llamada de Autocorrección almacenada por el mensaje [**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , siempre que el texto que precede al punto de inserción sea un candidato para la corrección automática.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Carácter de tipo **WCHAR**. Si este carácter es una tabulación (U + 0009) y el carácter que precede al punto de inserción no es una tabulación, el carácter que precede al punto de inserción se trata como parte de la cadena candidata de Autocorrección en lugar de como un delimitador de cadena. de lo contrario, *wParam* no tiene ningún efecto.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero si el mensaje se realiza correctamente, o es distinto de cero si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 





