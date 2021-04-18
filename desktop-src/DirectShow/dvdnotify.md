---
description: El evento DVDNotify notifica a una aplicación de muchos eventos de DVD e instrucciones de disco diferentes.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680443"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDNotify` evento notifica a una aplicación de muchos eventos de DVD e instrucciones de disco diferentes.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Especifica el código de notificación de eventos de DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Parámetro1*
</dt> <dd>

Puede contener información adicional relacionada con el evento.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Puede contener información adicional relacionada con el evento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los [códigos de notificación de eventos de DVD](dvd-notification-codes.md) proporcionan una explicación completa de todos los códigos de notificación de eventos de DVD y sus parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



 

 




