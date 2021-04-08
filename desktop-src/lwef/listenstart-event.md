---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903796"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando comienza el modo de escucha (reconocimiento de voz).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent. * * * ListenStart (ByVal* *  *CharacterID ** * *)*



| Parte          | Descripción                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de escucha como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento se envía a todos los clientes cuando comienza el modo de escucha porque el usuario presionó la clave de escucha o el cliente de entrada-activo llamó al método [**Listen**](listen-method.md) con **true**. Puede usar este evento para evitar que el personaje hable mientras el modo de escucha está activado.

Si activa el modo de escucha con el método [**Listen**](listen-method.md) y el usuario presiona la tecla de escucha, el modo de escucha se restablece y continúa hasta que se completa el tiempo de espera de la clave de escucha, se libera la clave de escucha o el usuario termina de hablar, lo que sea posterior. En esta situación, cuando el modo de escucha ya está activado, no recibirá un evento **ListenStart** adicional cuando el usuario presione la tecla de escucha.

El evento devuelve el carácter a los clientes que actualmente tienen este carácter cargado. El resto de clientes reciben un carácter nulo (cadena vacía).

### <a name="see-also"></a>Consulte también

[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)


 

 




