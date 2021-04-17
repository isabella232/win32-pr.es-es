---
title: Mensaje de WM_INITMENU (Winuser. h)
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
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714631"
---
# <a name="wm_initmenu-message"></a>Mensaje de INITMENU de WM \_

Se envía cuando un menú está a punto de activarse. Se produce cuando el usuario hace clic en un elemento de la barra de menús o presiona una tecla de menú. Esto permite que la aplicación modifique el menú antes de que se muestre.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

## <a name="remarks"></a>Observaciones

Un mensaje de **\_ INITMENU de WM** se envía solo cuando se tiene acceso por primera vez a un menú; solo se genera un mensaje de **WM \_ INITMENU** para cada acceso. Por ejemplo, al mover el mouse por varios elementos de menú mientras mantiene presionado el botón no se generan mensajes nuevos. **WM \_ INITMENU** no proporciona información sobre los elementos de menú.

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

[**INITMENUPOPUP de WM \_**](wm-initmenupopup.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

