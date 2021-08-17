---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74c59e05e021fdff05ee8991c4563a7a4be918f6ecb244c26402b5234b240b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105151"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera los datos de todas [**las**](command-event.md) alternativas de comando que se pasan a una devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Dirección de una variable que recibe los ID de [**comandos pasados**](command-event.md) a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Dirección de una variable que recibe las puntuaciones de confianza para [**las alternativas**](command-event.md) de comando pasadas a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Dirección de una variable que recibe el texto de voz para [**las alternativas**](command-event.md) de comando que se pasan a la devolución de llamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> </dl>

Si la entrada de voz desencadena [**IAgentNotifySink::Command**](iagentnotifysink--command.md), el servidor devuelve la mejor coincidencia, la segunda mejor coincidencia y la tercera mejor coincidencia, si las proporciona el motor de voz. Proporciona las puntuaciones de confianza relativas, en el intervalo de -100 a 100, y texto real "oído" por el motor de voz. Si la mejor coincidencia era un comando proporcionado por el servidor, el servidor envía un identificador NULL, pero sigue envía una puntuación de confianza y el [**texto de**](voice-property.md) voz.

Si la entrada de voz no era el origen del evento; Por ejemplo, si el usuario seleccionó el comando en el menú emergente del [](command-event.md) carácter, el servidor de Microsoft Agent devuelve el identificador del comando seleccionado, con una puntuación de confianza de 100 y texto de voz como NULL. Las otras alternativas devuelven como NULL con puntuaciones de confianza de cero (0) y texto de voz como NULL.

> [!Note]  
> No todos los motores de reconocimiento de voz pueden devolver todos los valores de todos los parámetros de este evento. Consulte con el proveedor del motor para determinar si el motor admite la interfaz Speech API Microsoft para devolver alternativas y puntuaciones de confianza.

 

## <a name="see-also"></a>Consulte también

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)


 

 




