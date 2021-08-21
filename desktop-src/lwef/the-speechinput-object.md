---
title: El objeto SpeechInput
description: El objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975525"
---
# <a name="the-speechinput-object"></a>El objeto SpeechInput

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El [**objeto SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) proporciona acceso a las propiedades de entrada de voz que mantiene el servidor del Agente . Las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent. El servidor devuelve valores solo si se ha instalado un motor de voz compatible y está habilitado.

Las [**propiedades Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)y [**Language**](https://www.bing.com/search?q=**Language**) ya no se admiten, pero (por compatibilidad con versiones anteriores) devuelven valores NULL si se consultan. Para consultar o establecer el modo de un reconocimiento de voz, use la [**propiedad SRModeID.**](srmodeid-property.md)

-   [Propiedades de SpeechInput](speechinput-properties.md)

 

 




