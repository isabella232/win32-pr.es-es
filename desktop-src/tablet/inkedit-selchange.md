---
description: Se produce cuando cambia la selección actual de texto en el control InkEdit o se mueve el punto de inserción.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648471"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit. SelChange

Se produce cuando cambia la selección actual de texto en el control [InkEdit](inkedit-control-reference.md) o se mueve el punto de inserción.

## <a name="syntax"></a>Sintaxis


```C++
void SelChange();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Puede usar el evento **SelChange** para comprobar las distintas propiedades que proporcionan información sobre la selección actual (como [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) para que pueda actualizar los botones de una barra de herramientas, por ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




