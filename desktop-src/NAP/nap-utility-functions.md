---
title: Funciones de la utilidad NAP
description: Las siguientes funciones de utilidad admiten la API de NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775336"
---
# <a name="nap-utility-functions"></a>Funciones de la utilidad NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las siguientes funciones de utilidad admiten la API de NAP.

Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y el asignador de memoria COM (CoTaskMemAlloc y CoTaskMemFree).

-   IN Parameters: se asigna y libera por el autor de la llamada.
-   Parámetros OUT (asignados por el destinatario) liberados por el llamador mediante CoTaskMem \* ()
-   Parámetros IN/OUT: asignados por el autor de la llamada, liberados y reasignados por el destinatario, que en última instancia ha liberado el llamador, mediante CoTaskMem \* ()

En las funciones FreeXxx (), también se liberarán todos los punteros incrustados.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




