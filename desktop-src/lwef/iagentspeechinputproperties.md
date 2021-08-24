---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660848eae85465ea322bcb08a218c6ee463eb384d3a4766cacf6a86038662386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609335"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

IAgentSpeechInputProperties proporciona acceso a las propiedades de entrada de voz que mantiene el servidor. La mayoría de las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent. El servidor de Microsoft Agent devuelve valores solo si se ha instalado un motor de voz compatible y está habilitado. La consulta de estas propiedades intenta iniciar el motor de voz.

**Métodos en orden de Vtable**



| Métodos IAgentSpeechInputProperties                                     | Descripción                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Devuelve si el motor de reconocimiento de voz está habilitado. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Devuelve la asignación de clave actual de la clave de escucha.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Devuelve si la sugerencia de escucha está habilitada.             |



 

[**Los métodos GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID,**](https://www.bing.com/search?q=**GetLCID**) [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)y [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (admitidos en versiones anteriores de Microsoft Agent) siguen siendo compatibles con versiones anteriores. Sin embargo, los métodos no tienen código auxiliar y no devuelven valores útiles. Use [**GetSRModeID y**](https://www.bing.com/search?q=**GetSRModeID**) [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar y establecer el motor de reconocimiento de voz que se usará con el carácter . Tenga en cuenta que el motor debe coincidir con la configuración de idioma actual del carácter.

 

 




