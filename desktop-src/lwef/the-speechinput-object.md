---
title: El objeto SpeechInput
description: El objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994382"
---
# <a name="the-speechinput-object"></a>El objeto SpeechInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El objeto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) proporciona acceso a las propiedades de entrada de voz mantenidas por el servidor del agente. Las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent. El servidor solo devuelve valores si se ha instalado un motor de voz compatible y está habilitado.

Ya no se admiten las propiedades [**Engine**](https://www.bing.com/search?q=**Engine**), [**installed**](https://www.bing.com/search?q=**Installed**)y [**Language**](https://www.bing.com/search?q=**Language**) , pero (por compatibilidad con versiones anteriores) devuelven valores NULL si se consultan. Para consultar o establecer el modo de reconocimiento de voz, use la propiedad [**SRModeID**](srmodeid-property.md) .

-   [Propiedades de SpeechInput](speechinput-properties.md)

 

 




