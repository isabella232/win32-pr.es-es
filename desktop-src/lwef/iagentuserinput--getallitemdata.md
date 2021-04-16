---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486534"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera los datos para todas las alternativas de [**comando**](command-event.md) que se pasan a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Dirección de una variable que recibe los identificadores de [**comandos**](command-event.md) pasados a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Dirección de una variable que recibe las puntuaciones de confianza para las alternativas de [**comando**](command-event.md) que se pasan a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Dirección de una variable que recibe el texto de la voz para las alternativas de [**comando**](command-event.md) que se pasan a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Si la entrada de voz desencadena [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), el servidor devuelve la mejor coincidencia, la segunda coincidencia mejor y la tercera coincidencia, si la proporciona el motor de voz. Proporciona las puntuaciones de confianza relativas, en el intervalo de-100 a 100 y el texto real "escuchado" por el motor de voz. Si la mejor coincidencia era un comando proporcionado por el servidor, el servidor envía un identificador nulo, pero todavía envía una puntuación de confianza y el texto de la [**voz**](voice-property.md) .

Si la entrada de voz no era el origen del evento; por ejemplo, si el usuario seleccionó el comando en el menú emergente del carácter, el servidor de agente de Microsoft devuelve el identificador del [**comando**](command-event.md) seleccionado, con una puntuación de confianza de 100 y el texto de voz como null. Las demás alternativas devuelven como NULL con puntuaciones de confianza de cero (0) y texto de voz como NULL.

> [!Note]  
> No todos los motores de reconocimiento de voz pueden devolver todos los valores de todos los parámetros de este evento. Consulte con el proveedor del motor para determinar si el motor es compatible con la interfaz de Microsoft Speech API para devolver alternativas y puntuaciones de confianza.

 

## <a name="see-also"></a>Consulte también

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md)


 

 




