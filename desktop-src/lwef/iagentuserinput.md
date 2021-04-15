---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420634"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Cuando el servidor notifica al cliente de entrada-activo con [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), devuelve información a través del objeto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) . **IAgentUserInput** define una interfaz que permite a las aplicaciones consultar estos valores.

**Métodos en orden de Vtable**



| Métodos IAgentUserInput                                         | Descripción                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Devuelve el número de alternativas de comando devueltas en un evento de [**comando**](command-event.md) .                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Devuelve el identificador de una alternativa de [**comando**](command-event.md) específica.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Devuelve el valor de la propiedad [**Confidence**](confidence-property.md) para una alternativa de [**comando**](command-event.md) concreta. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Devuelve el valor del texto de la [**voz**](voice-property.md) de una alternativa de [**comando**](command-event.md) específica.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Devuelve los datos para todas las alternativas de [**comando**](command-event.md) .                                                                  |



 

 

 