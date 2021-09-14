---
description: DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones de DDE entre aplicaciones que se ejecutan en equipos diferentes de una red.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Acerca de DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172333"
---
# <a name="about-network-dde"></a>Acerca de DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones de DDE entre aplicaciones que se ejecutan en equipos diferentes de una red. Una conversación *de* DDE es la interacción entre las aplicaciones cliente y servidor. El DDE de red se usa junto con DDE y la biblioteca de administración de DDE (DDEML) en la aplicación.

DDE es una forma de comunicación entre procesos que usa memoria compartida para intercambiar datos entre aplicaciones. Las aplicaciones pueden usar DDE para transferencias de datos únicas o para intercambios continuos y actualización de datos. Para obtener más información sobre DDE, [vea datos dinámicos Exchange](../dataxchg/dynamic-data-exchange.md).

DDEML simplifica la tarea de agregar la funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar mensajes DDE directamente, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones de DDE. Para obtener más información sobre DDEML, [vea datos dinámicos Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Archivos DDE de red

Para usar los elementos de API de DDE de red, debe incluir el archivo de encabezado NDDEApi.h en los archivos de origen e incluir el archivo NDDEApi.lib en la línea de vínculo. También debe asegurarse de que el NDDEApi.dll está cargado.

Para obtener más información, vea los temas siguientes:

-   [Agente DDE de red](network-dde-agent.md)
-   [Recursos compartidos de DDE](dde-shares.md)
-   [Seguridad y recursos compartidos de confianza](trusted-shares-and-security.md)
-   [Administración de recursos compartidos de DDE](managing-dde-shares.md)

 

 
