---
description: Una aplicación envía el mensaje de MDIDESTROY de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para cerrar una ventana secundaria MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Mensaje de WM_MDIDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809559"
---
# <a name="wm_mdidestroy-message"></a>Mensaje de MDIDESTROY de WM \_

Una aplicación envía el mensaje de **\_ MDIDESTROY de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para cerrar una ventana secundaria MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a cerrar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **cero**

Este mensaje siempre devuelve cero.

## <a name="remarks"></a>Observaciones

Este mensaje quita el título de la ventana secundaria MDI de la ventana de marco MDI y desactiva la ventana secundaria. Una aplicación debe usar este mensaje para cerrar todas las ventanas secundarias de MDI.

Si una ventana de cliente MDI recibe un mensaje que cambia la activación de sus ventanas secundarias y la ventana secundaria MDI activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MDICREATE de WM \_**](wm-mdicreate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




