---
title: TB_SETBUTTONSIZE mensaje (Commctrl.h)
description: Establece el tamaño de los botones de una barra de herramientas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE controles de Windows mensaje
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
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167738"
---
# <a name="tb_setbuttonsize-message"></a>Mensaje \_ DE TB SETBUTTONSIZE

Establece el tamaño de los botones de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el ancho, en píxeles, de los botones. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el alto, en píxeles, de los botones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

**TB \_ Por lo** general, se debe llamar a SETBUTTONSIZE después de agregar botones.

Use [**TB \_ SETBUTTONWIDTH para**](tb-setbuttonwidth.md) establecer el ancho máximo y mínimo permitido para los botones antes de agregarse. Use **TB \_ SETBUTTONSIZE para** establecer el tamaño real de los botones.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente establece el ancho de los botones en 80 píxeles y el alto en 30 píxeles.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

