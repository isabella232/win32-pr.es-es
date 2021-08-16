---
title: El objeto AudioOutput
description: El objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474955"
---
# <a name="the-audiooutput-object"></a>El objeto AudioOutput

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Este objeto proporciona acceso a las propiedades de salida de audio que mantiene el servidor. Las propiedades son de solo lectura, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent.

Si declara una variable de objeto de tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), no podrá acceder a todas las propiedades del [**objeto AudioOutput.**](/windows/desktop/lwef/the-audiooutput-object) Aunque el Agente también admite [**IAgentCtlAudioObject,**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)esta última interfaz solo se proporciona por compatibilidad con versiones anteriores y solo admite esas propiedades en versiones anteriores.

-   [**habilitado**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Estado**](status-property.md)

 

 