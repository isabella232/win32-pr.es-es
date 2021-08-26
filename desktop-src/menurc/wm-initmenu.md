---
title: WM_INITMENU mensaje (Winuser.h)
description: Se envía cuando un menú está a punto de activarse.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff775849abf6a7e3be4530ce893e1ae8821cb4be6e9fb2888ef9bb0ee6d67d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939575"
---
# <a name="wm_initmenu-message"></a>Mensaje \_ WM INITMENU

Se envía cuando un menú está a punto de activarse. Se produce cuando el usuario hace clic en un elemento de la barra de menús o presiona una tecla de menú. Esto permite a la aplicación modificar el menú antes de que se muestre.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del menú que se va a inicializar.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Un **mensaje \_ WM INITMENU** solo se envía cuando se accede por primera vez a un menú; solo se genera un mensaje **WM \_ INITMENU** para cada acceso. Por ejemplo, mover el mouse entre varios elementos de menú mientras se mantiene presionado el botón no genera nuevos mensajes. **WM \_ INITMENU no** proporciona información sobre los elementos de menú.

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

[**WM \_ INITMENUPOPUP**](wm-initmenupopup.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

