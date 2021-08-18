---
description: El método DVDTimeCode2bstr recupera una cadena que indica la hora actual en el disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bda68bafa462af5d425c62368b51f8b4b08ce2dfc310276e8f26b7c4601fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148608"
---
# <a name="dvdtimecode2bstr-method"></a>DVDTimeCode2bstr (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDTimeCode2bstr` método recupera una cadena que indica la hora actual en el disco.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Especifica la hora actual en el disco con respecto al inicio del título como un número obtenido a través del evento [**\_ EC DVD CURRENT \_ \_ HMSF \_ TIME.**](ec-dvd-current-hmsf-time.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena de 11 caracteres con el formato "hh:mm:ss:ff" que representa las horas, minutos, segundos y fotogramas que definen la hora actual.

## <a name="remarks"></a>Comentarios

Este método es de solo lectura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de notificaciones de eventos de DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



