---
description: Se produce cuando se quita un IInkTablet del sistema.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: Evento InkOverlay. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d0e69bae7cb6360794b9624fcef7c8be639e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648434"
---
# <a name="inkoverlaytabletremoved-event"></a>Evento InkOverlay. TabletRemoved

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

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Interfaz IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




