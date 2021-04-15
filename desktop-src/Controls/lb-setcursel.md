---
title: Mensaje de LB_SETCURSEL (Winuser. h)
description: Selecciona una cadena y la desplaza a la vista, si es necesario. Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105648157"
---
# <a name="lb_setcursel-message"></a>\_Mensaje lb SETCURSEL

Selecciona una cadena y la desplaza a la vista, si es necesario. Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero de la cadena seleccionada. Si este parámetro es-1, el cuadro de lista se establece para que no tenga ninguna selección.

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err. Si el parámetro *wParam* es-1, el valor devuelto es lb \_ Err aunque no se haya producido ningún error.

## <a name="remarks"></a>Observaciones

Use este mensaje solo con cuadros de lista de selección única. No se puede utilizar para establecer o quitar una selección en un cuadro de lista de selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





