---
description: Una aplicación envía el mensaje de MDIACTIVATE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active una ventana secundaria MDI diferente.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Mensaje de WM_MDIACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648389"
---
# <a name="wm_mdiactivate-message"></a>Mensaje de MDIACTIVATE de WM \_

Una aplicación envía el mensaje de **\_ MDIACTIVATE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para indicar a la ventana de cliente que active una ventana secundaria MDI diferente.


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

## <a name="remarks"></a>Observaciones

A medida que la ventana de cliente procesa este mensaje, envía **WM \_ MDIACTIVATE** a la ventana secundaria que se está desactivando y a la ventana secundaria que se va a activar. Los parámetros de mensaje recibidos por una ventana secundaria MDI son los siguientes:

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a desactivar.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Identificador de la ventana secundaria MDI que se va a activar.

</dd> </dl>

Una ventana secundaria MDI se activa independientemente de la ventana de marco MDI. Cuando la ventana de marco se activa, la ventana secundaria que se activó por última vez con el mensaje de **\_ MDIACTIVATE de WM** recibe el mensaje de [**\_ NCACTIVATE de WM**](wm-ncactivate.md) para dibujar un marco de ventana activo y una barra de título; la ventana secundaria no recibe otro mensaje de **\_ MDIACTIVATE de WM** .

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

[**MDIGETACTIVE de WM \_**](wm-mdigetactive.md)
</dt> <dt>

[**MDINEXT de WM \_**](wm-mdinext.md)
</dt> <dt>

[**NCACTIVATE de WM \_**](wm-ncactivate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




