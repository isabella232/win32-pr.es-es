---
description: Recupera la fuente con la que el control dibuja actualmente su texto.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: WM_GETFONT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d3dbd4a34557459fa0f31f6e2a96eba9d0cab36d54cf2bddaa353343a18b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200476"
---
# <a name="wm_getfont-message"></a>Mensaje \_ GETFONT de WM

Recupera la fuente con la que el control dibuja actualmente su texto.


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HFONT**

El valor devuelto es un identificador de la fuente utilizada por el control o **NULL** si el control usa la fuente del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ SETFONT**](wm-setfont.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




