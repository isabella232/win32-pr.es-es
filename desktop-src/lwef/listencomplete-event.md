---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d25e9bfbf23c6a2911c718b576c99395ef06fd802853b39b699384a9ab92429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883897"
---
# <a name="listencomplete-event"></a>Evento ListenComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando finaliza el modo de escucha (reconocimiento de voz).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent.:ListenComplete (ByVal* *  *CharacterID*, **ByVal** *Cause...))**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de escucha como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Causa*       | Devuelve la causa del evento completo como un entero que puede ser uno de los siguientes: 1 El código del programa ha desactivado el modo de escucha.<br/> 2 Se ha pasado el tiempo de espera del modo de escucha (activado por el código del programa).<br/> 3 Se ha pasado el tiempo de espera del modo de escucha (activado por la tecla De escucha).<br/> 4 El modo de escucha se ha desactivado porque el usuario ha liberado la clave de escucha.<br/> 5 El modo de escucha finalizó porque el usuario terminó de hablar.<br/> 6 El modo de escucha finalizó porque se desactivó el cliente activo de entrada.<br/> 7 El modo de escucha finalizó porque se cambió el carácter predeterminado.<br/> 8 El modo de escucha finalizó porque el usuario deshabilitó la entrada de voz.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento se envía a todos los clientes cuando finaliza el tiempo de espera del modo de escucha, una vez que el usuario libera la clave de escucha, cuando el cliente activo de entrada llama al método [**Listen**](listen-method.md) con **False** o el usuario termina de hablar. Puede usar este evento para determinar cuándo reanudar la salida de caracteres hablados (audio).

Si activa el modo de escucha mediante el método [**Listen**](listen-method.md) y, a continuación, el usuario presiona la tecla Escuchando, el modo de escucha se restablece y continúa hasta que se completa el tiempo de espera de la clave de escucha, se libera la tecla Listening o el usuario termina de hablar, lo que sea más adelante. En esta situación, no recibirá un evento **ListenComplete** hasta que se complete el modo de la clave de escucha.

El evento devuelve el carácter a los clientes que tienen este carácter cargado actualmente. Todos los demás clientes reciben un carácter nulo (cadena vacía).

### <a name="see-also"></a>Consulte también

[**Evento ListenStart,**](listenstart-event.md) [ **método Listen**](listen-method.md)


 

 





