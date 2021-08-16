---
description: Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Evento InkOverlay.SelectionChanging (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9b7fa52c4897c7e1152deff7636259e07e2768929223327243c2da0b59e362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218958"
---
# <a name="inkoverlayselectionchanging-event"></a>Evento InkOverlay.SelectionChanging

Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

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

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IOESelectionChanging.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Propiedad Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

