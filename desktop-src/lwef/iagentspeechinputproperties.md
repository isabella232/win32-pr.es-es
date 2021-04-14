---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418324"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

IAgentSpeechInputProperties proporciona acceso a las propiedades de entrada de voz mantenidas por el servidor. La mayoría de las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent. El servidor de agente de Microsoft solo devuelve valores si se ha instalado un motor de voz compatible y está habilitado. Al consultar estas propiedades se intenta iniciar el motor de voz.

**Métodos en orden de Vtable**



| Métodos IAgentSpeechInputProperties                                     | Descripción                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Devuelve si el motor de reconocimiento de voz está habilitado. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Devuelve la asignación de clave actual de la clave de escucha.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Devuelve si la sugerencia de escucha está habilitada.             |



 

Los métodos [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)y [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (que se admiten en versiones anteriores de Microsoft Agent) todavía se admiten por razones de compatibilidad con versiones anteriores. Sin embargo, los métodos no tienen stub y no devuelven valores útiles. Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) y [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar y establecer el motor de reconocimiento de voz que se va a usar con el carácter. Tenga en cuenta que el motor debe coincidir con la configuración de idioma actual del carácter.

 

 




