---
description: El evento DVDNotify notifica a una aplicación muchos eventos de DVD e instrucciones de disco diferentes.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148708"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDNotify` evento notifica a una aplicación muchos eventos de DVD diferentes e instrucciones de disco.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Especifica el código de notificación de eventos de DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Puede contener información adicional relacionada con el evento.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Puede contener información adicional relacionada con el evento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[Los códigos de notificación de eventos de DVD](dvd-notification-codes.md) dan una explicación completa de todos los códigos de notificación de eventos de DVD y sus parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




