---
description: Recupera el identificador de menú de la ventana actual.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Mensaje de MN_GETHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276885"
---
# <a name="mn_gethmenu-message"></a>MN \_ GETHMENU Message

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

Si se realiza correctamente, el valor devuelto es el **HMENU** de la ventana actual. Si se produce un error, el valor devuelto es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 




