---
description: Recupera el identificador de menú de la ventana actual.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: MN_GETHMENU mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cfc1eb6086f94f64e1a0e152e6f86fe89a0ea0278a6c4cc25a487edb6f93ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089935"
---
# <a name="mn_gethmenu-message"></a>Mensaje \_ GETHMENU de MN

Recupera el identificador de menú de la ventana actual.


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HMENU**

Si se realiza correctamente, el valor devuelto es **HMENU** para la ventana actual. Si se produce un error, el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 




