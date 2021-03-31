---
description: DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones DDE entre aplicaciones que se ejecutan en equipos diferentes en una red.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Acerca de DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360616"
---
# <a name="about-network-dde"></a>Acerca de DDE de red

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones DDE entre aplicaciones que se ejecutan en equipos diferentes en una red. Una *conversación* DDE es la interacción entre las aplicaciones cliente y servidor. El DDE de red se utiliza junto con DDE y la biblioteca de administración de DDE (DDEML) en la aplicación.

DDE es una forma de comunicación entre procesos que usa la memoria compartida para intercambiar datos entre aplicaciones. Las aplicaciones pueden utilizar DDE para transferencias de datos de una vez o para intercambios en curso y actualizar datos. Para obtener más información sobre DDE, consulte [intercambio dinámico de datos](../dataxchg/dynamic-data-exchange.md).

DDEML simplifica la tarea de agregar funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar directamente los mensajes DDE, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones DDE. Para obtener más información sobre DDEML, vea [biblioteca de administración de intercambio dinámico de datos](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Archivos DDE de red

Para usar los elementos de la API de DDE de red, debe incluir el archivo de encabezado NDDEApi. h en los archivos de código fuente e incluir el archivo NDDEApi. lib en la línea de vínculo. También debe asegurarse de que se carga el archivo de NDDEApi.dll.

Para obtener más información, vea los temas siguientes:

-   [Agente DDE de red](network-dde-agent.md)
-   [Recursos compartidos DDE](dde-shares.md)
-   [Seguridad y recursos compartidos de confianza](trusted-shares-and-security.md)
-   [Administrar recursos compartidos DDE](managing-dde-shares.md)

 

 
