---
title: EM_CALLAUTOCORRECTPROC mensaje (Richedit.h)
description: Llama a la función de devolución de llamada de autocorrección almacenada por el mensaje EM SETAUTOCORRECTPROC, siempre que el texto anterior al punto de inserción sea candidato para la \_ autocorrección.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC controles de Windows mensaje
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
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916085"
---
# <a name="em_callautocorrectproc-message"></a>Mensaje \_ EM CALLAUTOCORRECTPROC

Llama a la función de devolución de llamada de autocorrección almacenada por el mensaje [**\_ EM SETAUTOCORRECTPROC,**](em-setautocorrectproc.md) siempre que el texto anterior al punto de inserción sea candidato para la autocorrección.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Carácter de tipo **WCHAR.** Si este carácter es una pestaña (U+0009) y el carácter que precede al punto de inserción no es una pestaña, el carácter que precede al punto de inserción se trata como parte de la cadena candidata para autocorrección en lugar de como delimitador de cadena; de lo contrario, *wParam* no tiene ningún efecto.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero si el mensaje se realiza correctamente o distinto de cero si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





