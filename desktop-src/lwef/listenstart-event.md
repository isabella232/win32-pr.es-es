---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361202"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando comienza el modo de escucha (reconocimiento de voz).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent.**ListenStart (ByVal* *  *CharacterID...))**



| Parte          | Descripción                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de escucha como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento se envía a todos los clientes cuando comienza el modo de escucha porque el usuario presionó la tecla Listening o el cliente activo de entrada llamó al método [**Listen**](listen-method.md) con **True.** Puede usar este evento para evitar que el carácter hable mientras el modo de escucha está en funcionamiento.

Si activa el modo de escucha con el método [**Listen**](listen-method.md) y, a continuación, el usuario presiona la tecla Listening, el modo de escucha se restablece y continúa hasta que se complete el tiempo de espera de la clave listening, la tecla Listening se libera o el usuario termina de hablar, lo que sea más adelante. En esta situación, cuando el modo de escucha ya esté en funcionamiento, no recibirá un evento **ListenStart** adicional cuando el usuario presione la tecla Listening.

El evento devuelve el carácter a los clientes que tienen este carácter cargado actualmente. Todos los demás clientes reciben un carácter nulo (cadena vacía).

### <a name="see-also"></a>Consulte también

[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)


 

 




