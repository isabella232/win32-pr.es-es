---
description: 'Evento InkPicture.TabletRemoved: se produce cuando se quita un IInkTablet del sistema.'
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Evento InkPicture.TabletRemoved (Msmutut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f4fbd0839cb11d2da3fda65259b343934e866fc6fba08fb7d755799093fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844325"
---
# <a name="inkpicturetabletremoved-event"></a>Evento InkPicture.TabletRemoved

Se produce cuando [**se quita un IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TabletId* \[ En\]
</dt> <dd>

Valor long que se usó como identificador del objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que se quitó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de \_ DISPID ICETabletRemoved.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**IInkTablet (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




