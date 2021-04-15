---
description: El método DVDTimeCode2bstr recupera una cadena que indica la hora actual del disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Método DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677127"
---
# <a name="dvdtimecode2bstr-method"></a>Método DVDTimeCode2bstr

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDTimeCode2bstr` método recupera una cadena que indica la hora actual del disco.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Especifica la hora actual del disco con respecto al inicio del título como un número obtenido mediante el evento de [**\_ tiempo de \_ \_ HMSF actual \_ del DVD**](ec-dvd-current-hmsf-time.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena de 11 caracteres en el formato "HH: mm: SS: FF" que representa las horas, los minutos, los segundos y las tramas que definen la hora actual.

## <a name="remarks"></a>Observaciones

Este método es de solo lectura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de las notificaciones de eventos de DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



