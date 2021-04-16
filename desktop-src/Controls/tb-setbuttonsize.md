---
title: Mensaje de TB_SETBUTTONSIZE (commctrl. h)
description: Establece el tamaño de los botones de una barra de herramientas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658204"
---
# <a name="tb_setbuttonsize-message"></a>\_Mensaje SETBUTTONSIZE TB

Establece el tamaño de los botones de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho, en píxeles, de los botones. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el alto, en píxeles, de los botones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

**TB \_** Por lo general, se debe llamar a SETBUTTONSIZE después de agregar botones.

Use [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) para establecer los anchos máximo y mínimo permitidos para los botones antes de agregarlos. Use **TB \_ SETBUTTONSIZE** para establecer el tamaño real de los botones.

## <a name="examples"></a>Ejemplos

En el siguiente código de ejemplo se establece el ancho de los botones en 80 píxeles y el alto en 30 píxeles.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

