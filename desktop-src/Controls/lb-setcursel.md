---
title: LB_SETCURSEL mensaje (Winuser.h)
description: Selecciona una cadena y la desplaza a la vista, si es necesario. Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL controles de Windows mensaje
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
ms.openlocfilehash: b33964d98717ab84a325b5070eec6c4e1cacf334ba2272d4691d340a15af78a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085345"
---
# <a name="lb_setcursel-message"></a>Mensaje \_ DE LB SETCURSEL

Selecciona una cadena y la desplaza a la vista, si es necesario. Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero de la cadena seleccionada. Si este parámetro es -1, el cuadro de lista se establece para que no tenga ninguna selección.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR. Si el *parámetro wParam* es -1, el valor devuelto es \_ LB ERR aunque no se haya producido ningún error.

## <a name="remarks"></a>Comentarios

Use este mensaje solo con cuadros de lista de selección única. No se puede usar para establecer o quitar una selección en un cuadro de lista de selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





