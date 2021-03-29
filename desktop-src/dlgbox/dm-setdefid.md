---
title: Mensaje de DM_SETDEFID (Winuser. h)
description: Cambia el identificador del botón de opción predeterminado para un cuadro de diálogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID cuadros de diálogo de mensaje
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
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535265"
---
# <a name="dm_setdefid-message"></a>\_Mensaje SETDEFID de DM

Cambia el identificador del botón de opción predeterminado para un cuadro de diálogo.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de un control de botón de control que se convertirá en el valor predeterminado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto siempre es **true**.

## <a name="remarks"></a>Observaciones

Este mensaje lo procesa la función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) . Para establecer el botón de opción predeterminado, la función puede enviar mensajes [**WM \_ GETDLGCODE**](wm-getdlgcode.md) y [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) al control especificado y al botón de opción predeterminado actual.

El uso del mensaje **DM \_ SETDEFID** puede dar lugar a que aparezca más de un botón para que tenga el estado del botón de envío predeterminado. Cuando el sistema abre un cuadro de diálogo, dibuja el primer botón de opción de la plantilla de cuadro de diálogo con el borde de estado predeterminado. El envío de un mensaje **DM \_ SETDEFID** para cambiar el botón predeterminado no quitará siempre el borde de estado predeterminado del primer botón de la tecla de opción. En estos casos, la aplicación debe enviar un mensaje de [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) para cambiar el primer estilo de borde del botón de la tecla.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**GETDLGCODE de WM \_**](wm-getdlgcode.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](../controls/em-setlimittext.md)
</dt> </dl>

 

