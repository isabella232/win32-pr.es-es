---
title: EM_GETELLIPSISMODE mensaje (Richedit.h)
description: Recupera el modo de puntos suspensivos actual.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019703"
---
# <a name="em_getellipsismode-message"></a>Mensaje \_ EM GETVELOPSISMODE

Recupera el modo de puntos suspensivos actual. Cuando se habilita, se muestran los puntos suspensivos ( ) para el texto que no cabe en la ventana de presentación. Los puntos suspensivos solo se usan cuando el control no está activo. Cuando está activa, las barras de desplazamiento se usan para mostrar texto que no cabe en la ventana de presentación.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un DWORD que recibe uno de los valores siguientes.



| Value                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTOS \_ SUSPENSIVOS NINGUNO**</dt> </dl> | No se usan puntos suspensivos.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**FIN DE PUNTOS \_ SUSPENSIVOS**</dt> </dl>    | Puntos suspensivos al final (interrupción forzada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**PALABRA DE PUNTOS \_ SUSPENSIVOS**</dt> </dl> | Puntos suspensivos al final (salto de palabra).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si wparam es 0 y lparam no es NULL, el valor devuelto es TRUE; De lo contrario, el valor devuelto es FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ GETVELOPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





