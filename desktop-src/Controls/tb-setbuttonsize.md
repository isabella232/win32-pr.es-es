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
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166649"
---
# <a name="tb_setbuttonsize-message"></a>Mensaje \_ SETBUTTONSIZE de TB

Establece el tamaño de los botones de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el ancho, en píxeles, de los botones. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el alto, en píxeles, de los botones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

**TB \_ Por lo** general, se debe llamar a SETBUTTONSIZE después de agregar botones.

Use [**TB \_ SETBUTTONWIDTH para**](tb-setbuttonwidth.md) establecer los anchos máximos y mínimos permitidos para los botones antes de agregarse. Use **TB \_ SETBUTTONSIZE para** establecer el tamaño real de los botones.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente establece el ancho de los botones en 80 píxeles y el alto en 30 píxeles.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

