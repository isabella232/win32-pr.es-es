---
description: 'Evento InkOverlay.SelectionMoved: se produce cuando la posición de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay.SelectionMoved (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27bf1600683b5258bf899692b692c8cdcabb359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116873"
---
# <a name="inkoverlayselectionmoved-event"></a>Evento InkOverlay.SelectionMoved

Se produce cuando la posición de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Sintaxis


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldSelectionRect* \[ En\]
</dt> <dd>

Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal como existía antes de que se desencadenase el evento **SelectionMoved.**

> [!Note]  
> Este rectángulo se especifica en coordenadas de espacio de entrada manuscrita, lo que permite escenarios de deshacer.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El método de evento TThis se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IOESelectionMoved.

Para obtener el nuevo rectángulo delimitador de la colección de trazos que se han movido, llame al [**método Selection.GetBoundingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Propiedad Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle (clase)**](inkrectangle-class.md)
</dt> </dl>

 

