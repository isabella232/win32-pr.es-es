---
description: Una aplicación envía el mensaje WM MDIMAXIMIZE a una ventana cliente de interfaz de múltiples documentos (MDI) para maximizar \_ una ventana secundaria MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: WM_MDIMAXIMIZE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b187d4aed71d8582e4ea72686e30ee6339934a2bf6f5b4849fd8600c4a5552c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810515"
---
# <a name="wm_mdimaximize-message"></a>Mensaje \_ MDIMAXIMIZE de WM

Una aplicación envía el **mensaje \_ WM MDIMAXIMIZE** a una ventana cliente de interfaz de múltiples documentos (MDI) para maximizar una ventana secundaria MDI. El sistema cambia el tamaño de la ventana secundaria para que su área de cliente rellene la ventana de cliente. El sistema coloca el icono de menú de la ventana secundaria en la posición más a la derecha de la barra de menús de la ventana de marco y coloca el icono de restauración de la ventana secundaria en la posición más izquierda. El sistema también anexa el texto de la barra de título de la ventana secundaria al de la ventana de marco.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria de MDI que se va a maximizar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **cero**

El valor devuelto siempre es cero.

## <a name="remarks"></a>Comentarios

Si una ventana cliente MDI recibe algún mensaje que cambia la activación de sus ventanas secundarias mientras se maximiza la ventana secundaria MDI activa actualmente, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ MDIRESTORE**](wm-mdirestore.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




