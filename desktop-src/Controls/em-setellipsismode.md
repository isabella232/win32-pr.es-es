---
title: EM_SETELLIPSISMODE mensaje (Richedit.h)
description: Este mensaje establece el modo de puntos suspensivos actual.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445172ea0a4ed4ef49e9a131db8d4357faaa5f7fef553169b7a8e1e795fd01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019483"
---
# <a name="em_setellipsismode-message"></a>Mensaje \_ EM SETELLIPSISMODE

Este mensaje establece el modo de puntos suspensivos actual. Cuando se habilita, se muestran los puntos suspensivos ( ) para el texto que no cabe en la ventana de presentación. Los puntos suspensivos solo se usan cuando el control no está activo. Cuando está activa, las barras de desplazamiento se usan para mostrar texto que no cabe en la ventana de presentación.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

DWORD que recibe uno de los siguientes valores.



| Value                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTOS \_ SUSPENSIVOS NINGUNO**</dt> </dl> | No se usan puntos suspensivos.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**FIN DE PUNTOS \_ SUSPENSIVOS**</dt> </dl>    | Puntos suspensivos al final (interrupción forzada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**PALABRA DE PUNTOS \_ SUSPENSIVOS**</dt> </dl> | Puntos suspensivos al final (salto de palabra).<br/>   |



 

Todos los bits de estos valores caben en **ELLIPSIS \_ MASK**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si wparam es 0 y lparam es uno de los valores de la tabla anterior, el valor devuelto es TRUE; De lo contrario, el valor devuelto es FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETPSIPSISMODE**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ GETVELOPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





