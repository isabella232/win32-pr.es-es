---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976115"
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

**Sub** *agent.**ListenStart (ByVal* *  *CharacterID"))**



| Parte          | Descripción                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de escucha como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento se envía a todos los clientes cuando comienza el modo de escucha porque el usuario presionó la tecla Escuchando o el cliente activo de entrada llamó al método [**Listen**](listen-method.md) con **True**. Puede usar este evento para evitar que el carácter hable mientras el modo de escucha está en funcionamiento.

Si activa el modo de escucha con el método [**Listen**](listen-method.md) y, a continuación, el usuario presiona la tecla Escuchando, el modo de escucha se restablece y continúa hasta que se complete el tiempo de espera de la clave de escucha, se libera la tecla Listening o el usuario termina de hablar, lo que sea más adelante. En esta situación, cuando el modo de escucha ya está en funcionamiento, no recibirá un evento **ListenStart** adicional cuando el usuario presione la tecla Listening.

El evento devuelve el carácter a los clientes que tienen este carácter cargado actualmente. Todos los demás clientes reciben un carácter nulo (cadena vacía).

### <a name="see-also"></a>Consulte también

[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)


 

 




