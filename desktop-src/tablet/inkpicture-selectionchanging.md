---
description: Se produce cuando la selección de entrada de lápiz dentro del control InkPicture está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture.SelectionChanging (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256581"
---
# <a name="inkpictureselectionchanging-event"></a>Evento InkPicture.SelectionChanging

Se produce cuando la selección de entrada de lápiz dentro del control [InkPicture](inkpicture-control-reference.md) está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Sintaxis


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewSelection* \[ En\]
</dt> <dd>

Nueva colección de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que se está seleccionando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío (dispinterfaces) de **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ IOESelectionChanging.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Propiedad Selection \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

