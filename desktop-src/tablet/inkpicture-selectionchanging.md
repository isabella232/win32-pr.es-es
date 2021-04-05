---
description: Se produce cuando la selección de tinta dentro del control InkPicture está a punto de cambiar, por ejemplo, a través de las modificaciones a la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912906"
---
# <a name="inkpictureselectionchanging-event"></a>Evento InkPicture. SelectionChanging

Se produce cuando la selección de tinta dentro del control [InkPicture](inkpicture-control-reference.md) está a punto de cambiar, por ejemplo, a través de las modificaciones a la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .

## <a name="syntax"></a>Sintaxis


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewSelection* \[ de\]
</dt> <dd>

Nueva colección de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que se va a seleccionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOESelectionChanging.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

