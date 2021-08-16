---
title: Actualización desde la versión anterior
description: Actualización desde la versión anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745728"
---
# <a name="updating-from-previous-version"></a>Actualización desde la versión anterior

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Las aplicaciones compiladas y compiladas con la versión 1.5 anterior de Microsoft Agent deben ejecutarse sin modificaciones en la nueva versión 2.0. La [**propiedad Connected**](connected-property.md) ya no se puede establecer en **False**; Ciertas propiedades del objeto SpeechInput que se han reemplazado siguen existiendo, pero ya no convierten ningún valor, y el servidor ya no activa los eventos [**Restart**](https://www.bing.com/search?q=**Restart**) y [**Shutdown.**](https://www.bing.com/search?q=**Shutdown**)

Sin embargo, si actualiza las aplicaciones para que usen el control Agent 2.0, es posible que tenga que modificar el código. Si ha instalado la versión 2.0 de Microsoft Agent y ha cargado un proyecto de Visual Basic con la versión anterior del control agente, Visual Basic incluye una opción que mostrará automáticamente un mensaje que indica que ha detectado una nueva versión del control. Para garantizar el funcionamiento correcto de la aplicación, elija siempre usar la versión posterior.

Para otros lenguajes de programación (como Microsoft Office VBA 97), para actualizar el control, es posible que primero tenga que quitar el control del Agente 1.5 y guardar el código. A continuación, salga del entorno de programación, reinicie el entorno de programación, vuelva a cargar el código e inserte el nuevo control. Evite editar una aplicación habilitada para el Agente 2.0 en la misma instancia del entorno de programación en el que está editando una aplicación habilitada para el Agente 1.5. Es posible que algunos entornos de programación no controle las diferencias entre las dos versiones de los controles.

Debe poder desinstalar la versión del Agente 1.5 en el sistema después de instalar la versión del Agente 2.0. Sin embargo, si el Agente 1.5 está instalado en la versión 2.0, es posible que tenga que volver a instalar la versión 2.0.

 

 




