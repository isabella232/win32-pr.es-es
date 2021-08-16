---
description: Una aplicación envía el mensaje WM MDIACTIVATE a una ventana de cliente de interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active otra ventana secundaria \_ MDI.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: WM_MDIACTIVATE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b71e0f3755d76ecb44d60eecbd3b92c124aa59339a6fbf59a098b1eeb274f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931275"
---
# <a name="wm_mdiactivate-message"></a>Mensaje \_ MDIACTIVATE de WM

Una aplicación envía el **mensaje \_ WM MDIACTIVATE** a una ventana de cliente de interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active otra ventana secundaria MDI.


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a activar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación envía este mensaje a una ventana de cliente MDI, el valor devuelto es cero.

Una ventana secundaria MDI debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

A medida que la ventana de cliente procesa este mensaje, envía **WM \_ MDIACTIVATE** a la ventana secundaria que se está desactivando y a la ventana secundaria que se está activando. Los parámetros de mensaje recibidos por una ventana secundaria MDI son los siguientes:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Identificador de la ventana secundaria MDI que se está desactivando.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Identificador de la ventana secundaria MDI que se está activando.

</dd> </dl>

Una ventana secundaria MDI se activa independientemente de la ventana de marco MDI. Cuando la ventana de marco se activa, la ventana secundaria se activa por última vez mediante el mensaje **WM \_ MDIACTIVATE** recibe el mensaje [**WM \_ NCACTIVATE**](wm-ncactivate.md) para dibujar un marco de ventana activo y una barra de título; la ventana secundaria no recibe otro mensaje **\_ MDIACTIVATE** de WM.

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

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

[**WM \_ MDINEXT**](wm-mdinext.md)
</dt> <dt>

[**WM \_ NCACTIVATE**](wm-ncactivate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




