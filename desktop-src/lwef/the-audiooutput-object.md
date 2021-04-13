---
title: El objeto AudioOutput
description: El objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420710"
---
# <a name="the-audiooutput-object"></a>El objeto AudioOutput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Este objeto proporciona acceso a las propiedades de salida de audio mantenidas por el servidor. Las propiedades son de solo lectura, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent.

Si declara una variable de objeto de tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), no podrá tener acceso a todas las propiedades del objeto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Aunque el agente también admite [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), esta última interfaz se proporciona solo para la compatibilidad con versiones anteriores y solo admite esas propiedades en versiones anteriores.

-   [**habilitado**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Status**](status-property.md)

 

 