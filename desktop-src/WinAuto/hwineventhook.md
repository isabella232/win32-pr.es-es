---
title: HWINEVENTHOOK (Windef.h)
description: Se usa para declarar una función de enlace de eventos de ventana.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a26a2593af7db4520248b5ee319fd4143a79ab1393cef02365d1fe3ea8cc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994155"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Se usa para declarar una función de enlace de eventos de ventana.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Comentarios

Este tipo de datos se usa con la función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y las funciones [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y [**UnhookWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                          |
| Redistribuible<br/>          | Active Accessibility RDK 1.3 en Windows NT 4.0 con SP6 y versiones posteriores y Windows 95<br/>                                   |
| Header<br/>                   | <dl> <dt>Windef.h (WINVER >= 0x0500) (incluir Windows.h)</dt> </dl> |



 

 





