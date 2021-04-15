---
title: Actualizar desde la versión anterior
description: Actualizar desde la versión anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695246"
---
# <a name="updating-from-previous-version"></a>Actualizar desde la versión anterior

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Las aplicaciones compiladas y compiladas con la versión anterior 1,5 de Microsoft Agent deben ejecutarse sin modificaciones en la nueva versión 2,0. La propiedad [**Connected**](connected-property.md) ya no se puede establecer en **false**; algunas propiedades del objeto SpeechInput que se han reemplazado siguen existiendo, pero ya no convierten los valores y el servidor ya no desencadena los eventos de [**reinicio**](https://www.bing.com/search?q=**Restart**) y [**apagado**](https://www.bing.com/search?q=**Shutdown**) .

Sin embargo, si actualiza las aplicaciones para que usen el Control Agent 2,0, puede que tenga que modificar el código. Si ha instalado la versión 2,0 del agente de Microsoft y carga un proyecto de Visual Basic usa la versión anterior del control del agente, Visual Basic incluye una opción que muestra automáticamente un mensaje que indica que detectó una nueva versión del control. Para garantizar el correcto funcionamiento de la aplicación, elija usar siempre la versión más reciente.

En el caso de otros lenguajes de programación (como Microsoft Office VBA 97), para actualizar el control, puede que tenga que quitar primero el control del agente 1,5 y guardar el código. A continuación, salga del entorno de programación, reinicie el entorno de programación, vuelva a cargar el código e inserte el nuevo control. Evite la edición de una aplicación habilitada para el agente 2,0 en la misma instancia del entorno de programación en el que está editando una aplicación habilitada para el agente 1,5. Es posible que algunos entornos de programación no controlen las diferencias entre las dos versiones de los controles.

Debe poder desinstalar la versión del agente 1,5 en el sistema después de instalar la versión 2,0 del agente. Sin embargo, si el agente 1,5 está instalado en la versión 2,0, es posible que tenga que volver a instalar 2,0.

 

 




