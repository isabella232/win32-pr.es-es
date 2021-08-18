---
title: EM_SETAUTOCORRECTPROC mensaje (Richedit.h)
description: Define el procedimiento de devolución de llamada de autocorrección actual.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- EM_SETAUTOCORRECTPROC controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46e838cf18a345272b7983de1522a0c55a2565c5df3e11e3c89cd820653fb73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958724"
---
# <a name="em_setautocorrectproc-message"></a>Mensaje \_ EM SETAUTOCORRECTPROC

Define el procedimiento de devolución de llamada de autocorrección actual.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Función [*de devolución de llamada AutoCorrectProc.*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es cero. Si se produce un error en la operación, el valor devuelto es un valor distinto de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> </dl>

 

 





