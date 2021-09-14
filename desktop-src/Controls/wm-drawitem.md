---
title: WM_DRAWITEM mensaje (Winuser.h)
description: Se envía a la ventana primaria de un botón dibujado por el propietario, un cuadro combinado, un cuadro de lista o un menú cuando ha cambiado un aspecto visual del botón, cuadro combinado, cuadro de lista o menú.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165209"
---
# <a name="wm_drawitem-message"></a>Mensaje \_ DRAWITEM de WM

Se envía a la ventana primaria de un botón dibujado por el propietario, un cuadro combinado, un cuadro de lista o un menú cuando ha cambiado un aspecto visual del botón, cuadro combinado, cuadro de lista o menú.

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador del control que envió el **mensaje \_ DRAWITEM de WM.** Si un menú envió el mensaje, este parámetro es cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene información sobre el elemento que se va a dibujar y el tipo de dibujo necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**.

## <a name="remarks"></a>Observaciones

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dibuja el rectángulo de foco para un elemento de cuadro de lista dibujado por el propietario.

El *miembro itemAction* de la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica la operación de dibujo que debe realizar una aplicación.

Antes de volver del procesamiento de este mensaje, una aplicación debe asegurarse de que el contexto de dispositivo identificado por el *miembro hDC* de la estructura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está en el estado predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

