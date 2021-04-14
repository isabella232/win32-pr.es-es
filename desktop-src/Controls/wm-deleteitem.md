---
title: Mensaje de WM_DELETEITEM (Winuser. h)
description: Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado o cuando los elementos se quitan mediante el \_ mensaje lb DELETESTRING, lb \_ RESETCONTENT, CB \_ DELETESTRING o CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM controles de mensajes de Windows
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
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490366"
---
# <a name="wm_deleteitem-message"></a>Mensaje de WM \_ DELETEITEM

Se envía al propietario de un cuadro de lista o cuadro combinado cuando se destruye el cuadro de lista o el cuadro combinado o cuando los elementos se quitan mediante el mensaje [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT**](cb-resetcontent.md) . El sistema envía un mensaje de **WM \_ DELETEITEM** para cada elemento eliminado. El sistema envía el mensaje de **WM \_ DELETEITEM** para cualquier elemento de cuadro combinado o cuadro de lista eliminado con datos de elementos distintos de cero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el identificador del control que envió el mensaje de **WM \_ DELETEITEM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**deleteitemstruct (**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contiene información sobre el elemento eliminado de un cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver **true** si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Microsoft Windows NT y versiones posteriores: Windows envía un mensaje de **WM \_ DELETEITEM** solo para los elementos eliminados de un cuadro de lista dibujado por el propietario (con el estilo de la lbs de las [**libras \_**](list-box-styles.md) o el tipo [**\_ OwnerDrawVariable**](list-box-styles.md) ) o el cuadro combinado dibujado por el propietario (con el estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ).

Windows 95: Windows envía el mensaje de **WM \_ DELETEITEM** para cualquier elemento de cuadro combinado o cuadro de lista eliminado con datos de elementos distintos de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT (**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 





