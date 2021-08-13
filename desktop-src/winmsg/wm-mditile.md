---
description: Una aplicación envía el mensaje MDITILE de WM a una ventana de cliente de interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias MDI en \_ un formato de icono.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: WM_MDITILE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379394d413c0c9d15b9f63297934b97da6aff65b4ae5d803627cb0107493c4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436222"
---
# <a name="wm_mditile-message"></a>Mensaje \_ MDITILE de WM

Una aplicación envía el mensaje **\_ MDITILE** de WM a una ventana de cliente de interfaz de múltiples documentos (MDI) para organizar todas sus ventanas secundarias MDI en un formato de icono.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Opción de tiling. Este parámetro puede ser uno de los siguientes valores, combinado opcionalmente con **MDITILE \_ SKIPDISABLED** para evitar que las ventanas secundarias MDI deshabilitadas se en mosaico.



| Value                                                                                                                                                                                                                                    | Significado                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_ Horizontal**</dt> <dt>0x0001</dt> </dl> | Ventanas de iconos horizontalmente.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_ Vertical**</dt> <dt>0x0000</dt> </dl>       | Ventanas de iconos verticalmente.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Si el mensaje se realiza correctamente, el valor devuelto es **TRUE.**

Si se produce un error en el mensaje, el valor devuelto es **FALSE.**

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

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 




