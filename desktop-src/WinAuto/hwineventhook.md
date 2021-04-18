---
title: HWINEVENTHOOK (WINDEF. h)
description: Se usa para declarar una función de enlace de eventos de ventana.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695942"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Se usa para declarar una función de enlace de eventos de ventana.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Observaciones

Este tipo de datos se usa con la función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y las funciones [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                          |
| Redistribuible<br/>          | Active Accessibility 1,3 RDK en Windows NT 4,0 con SP6 y versiones posteriores y Windows 95<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WINDEF. h (WINVER >= 0x0500) (incluye Windows. h)</dt> </dl> |



 

 





