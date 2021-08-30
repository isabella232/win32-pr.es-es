---
description: El agente DDE de red inicia el DDE de red si detecta la actividad DDE de red local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c3958a8486f838a769191fabddb9c32f84b7af090f78b864a937bdb4f411f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963915"
---
# <a name="network-dde-agent"></a>Agente DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

El agente DDE de red inicia el DDE de red si detecta la actividad DDE de red local. No detecta un cliente remoto que intenta conectarse. Por lo tanto, para que cualquier cliente pueda conectarse correctamente, el DDE de red debe iniciarse en el equipo servidor. Tenga en cuenta que DDE de red no se inicia de forma predeterminada. Para iniciar DDE de red, ejecute NETDDE.EXE. Este archivo se encuentra en el directorio Windows usuario.

El agente DDE de red también inicia las aplicaciones necesarias para DDE de red. Una vez iniciada la DDE de red, las conversaciones de DDE se controlan a través de una ventana DDE de red asociada a una de las aplicaciones DDE de red. Esta aplicación actúa como proxy. Se comunica con todas las aplicaciones DDE locales y remotas.

 

 



