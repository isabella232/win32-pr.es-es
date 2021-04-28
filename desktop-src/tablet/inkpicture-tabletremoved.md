---
description: 'Evento InkPicture.TabletRemoved: se produce cuando se quita un IInkTablet del sistema.'
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Evento InkPicture.TabletRemoved (Msmutut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929458c6b972143852b5921a8c8364a54a4b6f41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113654"
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

Este método de evento se define en las interfaces de solo envío (dispinterfaces) **\_ de IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ ICETabletRemoved.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**IInkTablet (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




