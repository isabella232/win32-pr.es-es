---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419060"
---
# <a name="listencomplete-event"></a>Evento ListenComplete

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Tiene lugar cuando el modo de escucha (reconocimiento de voz) ha finalizado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent. * * * ListenComplete (ByVal* *  *CharacterID*, **ByVal** *causa * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de escucha como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Causa*       | Devuelve la causa del evento completo como un entero que puede ser uno de los siguientes: 1 modo de escucha desactivado por el código del programa.<br/> 2 el modo de escucha (activado por el código del programa) agotó el tiempo de espera.<br/> 3 el modo de escucha (activado por la clave de escucha) agotó el tiempo de espera.<br/> 4 el modo de escucha estaba desactivado porque el usuario liberó la clave de escucha.<br/> 5 modo de escucha finalizado porque el usuario terminó de hablar.<br/> 6 modo de escucha finalizado porque el cliente de entrada-activo se desactivó.<br/> 7 el modo de escucha finalizó porque se cambió el carácter predeterminado.<br/> 8 el modo de escucha ha finalizado porque el usuario ha deshabilitado la entrada de voz.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento se envía a todos los clientes cuando finaliza el tiempo de espera del modo de escucha, una vez que el usuario libera la clave de escucha, cuando el cliente activo de entrada llama al método [**Listen**](listen-method.md) con **false** o el usuario ha terminado de hablar. Puede usar este evento para determinar cuándo se debe reanudar la salida de caracteres hablados (audio).

Si activa el modo de escucha mediante el método de [**escucha**](listen-method.md) y, a continuación, el usuario presiona la tecla de escucha, el modo de escucha se restablece y continúa hasta que se completa el tiempo de espera de la clave de escucha, se libera la clave de escucha o el usuario termina de hablar, lo que sea posterior. En esta situación, no recibirá un evento **ListenComplete** hasta que se complete el modo de la clave de escucha.

El evento devuelve el carácter a los clientes que actualmente tienen este carácter cargado. El resto de clientes reciben un carácter nulo (cadena vacía).

### <a name="see-also"></a>Consulte también

[**Evento ListenStart**](listenstart-event.md), [ **método Listen**](listen-method.md)


 

 





