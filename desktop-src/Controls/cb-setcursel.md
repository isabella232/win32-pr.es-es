---
title: Mensaje de CB_SETCURSEL (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETCURSEL para seleccionar una cadena en la lista de un cuadro combinado.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079355"
---
# <a name="cb_setcursel-message"></a>\_Mensaje SETCURSEL CB

Una aplicación envía un mensaje **CB \_ SETCURSEL** para seleccionar una cadena en la lista de un cuadro combinado. Si es necesario, la lista desplaza la cadena a la vista. El texto del control de edición del cuadro combinado cambia para reflejar la nueva selección, y se quita cualquier selección anterior en la lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero de la cadena que se va a seleccionar. Si este parámetro es-1, se quita cualquier selección actual de la lista y se borra el control de edición.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice del elemento seleccionado. Si *wParam* es mayor que el número de elementos de la lista o si *wParam* es-1, el valor devuelto es CB \_ Err y se borra la selección.

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> </dl>

 

 





