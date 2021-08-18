---
title: WM_DELETEITEM mensaje (Winuser.h)
description: Se envía al propietario de un cuadro de lista o cuadro combinado cuando el cuadro de lista o el cuadro combinado se destruyen o cuando los elementos se quitan mediante el mensaje LB \_ DELETESTRING, LB \_ RESETCONTENT, CB DELETESTRING o \_ CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f461b63d751822d9a4c602993314bf0677cff754881269ab44458ab17f3a439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018543"
---
# <a name="wm_deleteitem-message"></a>Mensaje \_ DELETEITEM de WM

Se envía al propietario de un cuadro de lista o cuadro combinado cuando el cuadro de lista o el cuadro combinado se destruyen o cuando los elementos se quitan mediante el mensaje [**LB \_ DELETESTRING,**](lb-deletestring.md) [**LB \_ RESETCONTENT,**](lb-resetcontent.md) [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT.**](cb-resetcontent.md) El sistema envía un **mensaje \_ DELETEITEM de WM** para cada elemento eliminado. El sistema envía el mensaje **\_ DELETEITEM de WM** para cualquier cuadro de lista eliminado o elemento de cuadro combinado con datos de elementos distintos de cero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador del control que envió el **mensaje \_ DELETEITEM de WM.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contiene información sobre el elemento eliminado de un cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver **TRUE** si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Microsoft Windows NT y versiones posteriores: Windows envía un mensaje **\_ DELETEITEM** wm solo para los elementos eliminados de un cuadro de lista dibujado por el propietario (con el estilo [**\_ OWNERDRAWFIXED**](list-box-styles.md) o [**LBS \_ OWNERDRAWVARIABLE)**](list-box-styles.md) o el cuadro combinado dibujado por el propietario (con el estilo [**\_ CBS OWNERDRAWFIXED**](combo-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE).**](combo-box-styles.md)

Windows 95: Windows envía el mensaje **\_ DELETEITEM** de WM para cualquier cuadro de lista eliminado o elemento de cuadro combinado con datos de elementos distintos de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 





