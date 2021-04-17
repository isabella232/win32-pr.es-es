---
description: Una aplicación envía el mensaje de MDIGETACTIVE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para recuperar el identificador de la ventana secundaria MDI activa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Mensaje de WM_MDIGETACTIVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706665"
---
# <a name="wm_mdigetactive-message"></a>Mensaje de MDIGETACTIVE de WM \_

Una aplicación envía el mensaje de **\_ MDIGETACTIVE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para recuperar el identificador de la ventana secundaria MDI activa.


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

Estado maximizado. Si este parámetro no es **null**, es un puntero a un valor que indica el estado maximizado de la ventana secundaria MDI. Si el valor es **true**, la ventana está maximizada; un valor de **false** indica que no lo es. Si este parámetro es **null**, se omite el parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **hWnd**

El valor devuelto es el identificador de la ventana secundaria MDI activa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre la interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




