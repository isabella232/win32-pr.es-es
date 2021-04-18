---
description: La clase CAMMsgEvent es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Clase CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671051"
---
# <a name="cammsgevent-class"></a>Clase CAMMsgEvent

![jerarquía de clases cammsgevent](images/util06.png)

La `CAMMsgEvent` clase es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.

Esta clase se deriva del objeto [**CAMEvent**](camevent.md) . Agrega un método, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), que envía los mensajes entrantes mientras se espera.



| Métodos públicos                                 | Descripción                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Constructor.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Espera a que se señale el evento y envía los mensajes enviados. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




