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
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062134"
---
# <a name="em_setautocorrectproc-message"></a>Mensaje \_ SETAUTOCORRECTPROC de EM

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> </dl>

 

 





