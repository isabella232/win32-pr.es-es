---
description: Se envía a la ventana primaria de un menú o control dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969474"
---
# <a name="dfm_wm_drawitem-message"></a>Mensaje \_ DRAWITEM de WM DE DFM \_

Se envía a la ventana primaria de un menú o control dibujado por el propietario cuando ha cambiado un aspecto visual del control o menú.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Identificador del control que envió el **mensaje \_ DFM WM \_ DRAWITEM.** Si un menú envió el mensaje, este parámetro es cero.

</dd> <dt>

*lpDrawItem* \[ out\]
</dt> <dd>

Puntero a una [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento que se va a dibujar y el tipo de dibujo necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**.

## <a name="remarks"></a>Comentarios

El **miembro itemAction** de la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica la operación de dibujo que debe realizar una aplicación.

Antes de volver del procesamiento de este mensaje, una aplicación debe asegurarse de que el contexto de dispositivo identificado por el **miembro hDC** de la estructura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está en el estado predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
