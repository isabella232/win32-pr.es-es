---
description: Se produce cuando se quita un IInkTablet del sistema.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: InkCollector. TabletRemoved evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec723a6752f79a1a1d56d318d49ec3d025919d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715081"
---
# <a name="inkcollectortabletremoved-event"></a>InkCollector. TabletRemoved, evento

Se produce cuando se quita un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TabletId* \[ de\]
</dt> <dd>

Valor Long que se usó como identificador para el objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se ha quitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICETabletRemoved.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**Interfaz IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




