---
title: Mensaje EM_SETELLIPSISMODE (RichEdit. h)
description: Este mensaje establece el modo de puntos suspensivos actual.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE controles de mensajes de Windows
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
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079662"
---
# <a name="em_setellipsismode-message"></a>\_Mensaje SETELLIPSISMODE em

Este mensaje establece el modo de puntos suspensivos actual. Cuando está habilitada, se muestra un botón de puntos suspensivos () para el texto que no cabe en la ventana de presentación. Los puntos suspensivos solo se usan cuando el control no está activo. Cuando está activo, las barras de desplazamiento se utilizan para mostrar el texto que no cabe en la ventana de presentación.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

DWORD que recibe uno de los valores siguientes.



| Value                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**puntos suspensivos \_ ninguno**</dt> </dl> | No se usa ningún botón de puntos suspensivos.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**fin de los puntos suspensivos \_**</dt> </dl>    | Puntos suspensivos al final (interrupción forzada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**Palabra de puntos suspensivos \_**</dt> </dl> | Puntos suspensivos al final (salto de palabra).<br/>   |



 

Los bits de estos valores caben en la **\_ máscara de puntos suspensivos**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si wParam es 0 y lParam es uno de los valores de la tabla anterior, el valor devuelto es igual a TRUE. de lo contrario, el valor devuelto es igual a FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETELLIPSISMODE em**](em-getellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





