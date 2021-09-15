---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570640"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Cuando el servidor notifica al cliente activo de entrada con [**IAgentNotifySink::Command**](iagentnotifysink--command.md), devuelve información a través del [**objeto IAgentUserInput.**](/windows/desktop/lwef/iagentuserinput) **IAgentUserInput** define una interfaz que permite a las aplicaciones consultar estos valores.

**Métodos en orden de Vtable**



| Métodos IAgentUserInput                                         | Descripción                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Devuelve el número de alternativas de comando devueltas en un [**evento Command.**](command-event.md)                                         |
| [**GetItemID**](iagentuserinput--getitemid.md)                 | Devuelve el identificador de una alternativa [**de comando**](command-event.md) específica.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Devuelve el valor de la [**propiedad Confidence**](confidence-property.md) para una alternativa [**de comando**](command-event.md) específica. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Devuelve el valor de Texto [**de**](voice-property.md) voz para una alternativa [**de comando**](command-event.md) específica.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Devuelve los datos de todas las [**alternativas**](command-event.md) de comando.                                                                  |



 

 

 