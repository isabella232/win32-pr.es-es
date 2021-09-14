---
title: CB_SETCURSEL mensaje (Winuser.h)
description: Una aplicación envía un mensaje \_ CB SETCURSEL para seleccionar una cadena en la lista de un cuadro combinado.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174173"
---
# <a name="cb_setcursel-message"></a>Mensaje \_ DE CB SETCURSEL

Una aplicación envía un **mensaje \_ CB SETCURSEL** para seleccionar una cadena en la lista de un cuadro combinado. Si es necesario, la lista desplaza la cadena a la vista. El texto del control de edición del cuadro combinado cambia para reflejar la nueva selección y se quita cualquier selección anterior de la lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero de la cadena que se debe seleccionar. Si este parámetro es -1, se quita cualquier selección actual de la lista y se borra el control de edición.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice del elemento seleccionado. Si *wParam es* mayor que el número de elementos de la lista o *si wParam* es -1, el valor devuelto es CB ERR y la selección se \_ borra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

 





