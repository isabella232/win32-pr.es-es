---
description: Una aplicación envía el mensaje WM MDIDESTROY a una ventana de cliente de interfaz de múltiples documentos \_ (MDI) para cerrar una ventana secundaria MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232514831defe3c65cdce66a5e1c7348ad4f80508eb01615572b7aa5b7d8e9c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772066"
---
# <a name="wm_mdidestroy-message"></a>Mensaje \_ MDIDESTROY de WM

Una aplicación envía el **mensaje \_ WM MDIDESTROY** a una ventana de cliente de interfaz de múltiples documentos (MDI) para cerrar una ventana secundaria MDI.


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

## <a name="remarks"></a>Comentarios

Este mensaje quita el título de la ventana secundaria MDI de la ventana marco MDI y desactiva la ventana secundaria. Una aplicación debe usar este mensaje para cerrar todas las ventanas secundarias MDI.

Si una ventana cliente MDI recibe un mensaje que cambia la activación de sus ventanas secundarias y la ventana secundaria MDI activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ MDICREATE**](wm-mdicreate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




