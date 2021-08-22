---
title: Funciones de la utilidad NAP
description: Las siguientes funciones de utilidad admiten la API nap.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620786"
---
# <a name="nap-utility-functions"></a>Funciones de la utilidad NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las siguientes funciones de utilidad admiten la API nap.

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y el asignador de memoria COM (CoTaskMemAlloc y CoTaskMemFree).

-   Parámetros IN: asignados y liberados por el autor de la llamada.
-   Parámetros OUT: asignados por destinatario, que el autor de la llamada libera mediante CoTaskMem \* ()
-   Parámetros IN/OUT: asignados por el autor de la llamada, liberadas y reasignadas por el destinatario, liberadas en última instancia por el autor de la llamada, mediante CoTaskMem \* ()

En las funciones FreeXxx(), también se liberarán todos los punteros incrustados.

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

 

 




