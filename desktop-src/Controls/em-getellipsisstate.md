---
title: Mensaje EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera el estado de los puntos suspensivos actuales.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- EM_GETELLIPSISSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490726"
---
# <a name="em_getellipsisstate-message"></a>\_Mensaje GETELLIPSISSTATE em

Recupera el estado de los puntos suspensivos actuales.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es TRUE si se muestran puntos suspensivos y FALSE en caso contrario.

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

[**\_SETELLIPSISMODE em**](em-setellipsismode.md)
</dt> </dl>

 

 





