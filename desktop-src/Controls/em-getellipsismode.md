---
title: Mensaje EM_GETELLIPSISMODE (RichEdit. h)
description: Recupera el modo de puntos suspensivos actual.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE controles de mensajes de Windows
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
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150321"
---
# <a name="em_getellipsismode-message"></a>\_Mensaje GETELLIPSISMODE em

Recupera el modo de puntos suspensivos actual. Cuando está habilitada, se muestra un botón de puntos suspensivos () para el texto que no cabe en la ventana de presentación. Los puntos suspensivos solo se usan cuando el control no está activo. Cuando está activo, las barras de desplazamiento se utilizan para mostrar el texto que no cabe en la ventana de presentación.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un valor DWORD que recibe uno de los valores siguientes.



| Value                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**puntos suspensivos \_ ninguno**</dt> </dl> | No se usa ningún botón de puntos suspensivos.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**fin de los puntos suspensivos \_**</dt> </dl>    | Puntos suspensivos al final (interrupción forzada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**Palabra de puntos suspensivos \_**</dt> </dl> | Puntos suspensivos al final (salto de palabra).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si wParam es 0 y lParam no es NULL, el valor devuelto es igual a TRUE; de lo contrario, el valor devuelto es igual a FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETELLIPSISMODE em**](em-setellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





