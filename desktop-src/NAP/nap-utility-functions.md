---
title: Funciones de la utilidad NAP
description: Las siguientes funciones de utilidad admiten la API nap.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161245"
---
# <a name="nap-utility-functions"></a>Funciones de la utilidad NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las siguientes funciones de utilidad admiten la API nap.

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y el asignador de memoria COM (CoTaskMemAlloc y CoTaskMemFree).

-   Parámetros IN: asignados y liberados por el autor de la llamada.
-   Parámetros OUT: asignados por destinatario, que libera el autor de la llamada mediante CoTaskMem \* ()
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

 

 




