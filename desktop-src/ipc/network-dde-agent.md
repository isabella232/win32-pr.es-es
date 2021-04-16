---
description: El agente DDE de red inicia DDE de red si detecta la actividad DDE de red local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686524"
---
# <a name="network-dde-agent"></a>Agente DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

El agente DDE de red inicia DDE de red si detecta la actividad DDE de red local. No detecta un cliente remoto que intente conectarse. Por lo tanto, antes de que un cliente pueda conectarse correctamente, se debe iniciar DDE de red en el equipo servidor. Tenga en cuenta que DDE de red no se inicia de forma predeterminada. Para iniciar DDE de red, ejecute NETDDE.EXE. Este archivo se encuentra en el directorio de Windows.

El agente DDE de red también inicia las aplicaciones necesarias para DDE de red. Una vez iniciado DDE de red, las conversaciones DDE se controlan a través de una ventana DDE de red asociada a una de las aplicaciones DDE de red. Esta aplicación actúa como proxy. Se comunica con todas las aplicaciones DDE locales y remotas.

 

 



