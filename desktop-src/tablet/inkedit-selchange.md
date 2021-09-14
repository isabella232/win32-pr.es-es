---
description: Se produce cuando la selección actual de texto en el control InkEdit ha cambiado o se ha movido el punto de inserción.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit.SelChange (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256677"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit.SelChange

Se produce cuando la selección actual de texto en el control [InkEdit](inkedit-control-reference.md) ha cambiado o se ha movido el punto de inserción.

## <a name="syntax"></a>Sintaxis


```C++
void SelChange();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Puede usar el evento **SelChange** para comprobar las distintas propiedades que dan información sobre la selección actual (por [**ejemplo, SelBold)**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)para poder actualizar los botones de una barra de herramientas, por ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




