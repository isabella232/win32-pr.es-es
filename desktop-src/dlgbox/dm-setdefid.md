---
title: DM_SETDEFID mensaje (Winuser.h)
description: Cambia el identificador del botón de inserción predeterminado de un cuadro de diálogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID cuadros de diálogo del mensaje
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741755"
---
# <a name="dm_setdefid-message"></a>Mensaje \_ SETDEFID de DM

Cambia el identificador del botón de inserción predeterminado de un cuadro de diálogo.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de un control de botón de inserción que se convertirá en el valor predeterminado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **TRUE.**

## <a name="remarks"></a>Comentarios

La función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) procesa este mensaje. Para establecer el botón de inserción predeterminado, la función puede enviar mensajes [**\_ WM GETDLGCODE**](wm-getdlgcode.md) y [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) al control especificado y al botón de inserción predeterminado actual.

El uso **del \_ mensaje SETDEFID de DM** puede dar lugar a que más de un botón parezca tener el estado de botón de inserción predeterminado. Cuando el sistema abre un cuadro de diálogo, dibuja el primer botón de inserción de la plantilla de diálogo con el borde de estado predeterminado. El envío **de un \_ mensaje SETDEFID de DM** para cambiar el botón predeterminado no siempre quitará el borde de estado predeterminado del primer botón de inserción. En estos casos, la aplicación debe enviar un [**mensaje \_ BM SETSTYLE**](../controls/bm-setstyle.md) para cambiar el primer estilo de borde del botón de inserción.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**WM \_ GETDLGCODE**](wm-getdlgcode.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](../controls/em-setlimittext.md)
</dt> </dl>

 

