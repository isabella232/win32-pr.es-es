---
description: Una aplicación envía el mensaje MDIGETACTIVE de WM a una ventana cliente de interfaz de múltiples documentos (MDI) para recuperar el identificador a la ventana secundaria \_ de MDI activa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466505"
---
# <a name="wm_mdigetactive-message"></a>Mensaje \_ MDIGETACTIVE de WM

Una aplicación envía el **mensaje \_ MDIGETACTIVE** de WM a una ventana cliente de interfaz de múltiples documentos (MDI) para recuperar el identificador a la ventana secundaria de MDI activa.


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Estado maximizado. Si este parámetro no es **NULL,** es un puntero a un valor que indica el estado maximizado de la ventana secundaria MDI. Si el valor es **TRUE**, la ventana se maximiza; Un valor **de FALSE** indica que no lo es. Si este parámetro es **NULL,** se omite el parámetro .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HWND**

El valor devuelto es el identificador de la ventana secundaria MDI activa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción a la interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




