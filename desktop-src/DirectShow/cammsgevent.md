---
description: La clase CAMMsgEvent es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Clase CAMMsgEvent (Wxutil.h)
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
ms.openlocfilehash: c7c4d3c8268f06e81d1bd1a5285f7e4785459889397ccf249bbde7f0dd627f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955444"
---
# <a name="cammsgevent-class"></a>CLASE CAMMsgEvent

![jerarquía de clases de cammsgevent](images/util06.png)

La `CAMMsgEvent` clase es un contenedor para los objetos de evento que realizan el procesamiento de mensajes.

Esta clase se deriva del [**objeto CAMEvent.**](camevent.md) Agrega un método, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), que envía los mensajes entrantes mientras espera.



| Métodos públicos                                 | Descripción                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Constructor.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Espera a que se señale el evento, mientras se envían los mensajes enviados. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




