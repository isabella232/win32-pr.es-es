---
title: Cómo un servicio crea sus SPN
description: Un servicio puede usar dos funciones para componer sus SPN DsGetSpn es una función de uso general para la creación de SPN y DsServerRegisterSpn es una función especializada para crear y registrar SPN simples para un servicio basado en host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nombre de entidad de seguridad de servicio AD, cómo se compone un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903116"
---
# <a name="how-a-service-composes-its-spns"></a>Cómo un servicio crea sus SPN

Un servicio puede usar dos funciones para crear sus SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) es una función de uso general para la creación de SPN y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) es una función especializada para crear y registrar SPN simples para un servicio basado en host.

Un instalador de servicio suele usar la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear SPN, que después se registra en la cuenta de inicio de sesión del servicio mediante la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) . El **DsGetSpn** puede realizar las siguientes funciones.

-   Cree un SPN simple con el <service class> / <host> formato "" para un servicio basado en host.
-   Cree un SPN complejo que incluya el &lt; componente de "nombre de servicio &gt; " que usan los servicios replicables o el &lt; componente "Port &gt; " que distingue varias instancias de un servicio en un solo host.
-   Cree un único SPN con el &lt; componente "host &gt; " establecido en el nombre de un host especificado o en el nombre del equipo local de forma predeterminada.
-   Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en varios hosts de todo el bosque. Cada SPN especifica el nombre del host para una instancia de servicio.
-   Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en el mismo host. Cada SPN especifica el nombre del host y un número de puerto para una instancia de servicio.

La matriz de nombres devuelta por [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) debe liberarse llamando a la función [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .

Tenga en cuenta que las funciones [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) no comprueban que los SPN son únicos. Dado que se produce un error en la autenticación mutua si un cliente presenta un SPN que no es único, Compruebe la unicidad antes de registrar un SPN. Para ello, busque en el catálogo global (GC) los atributos **ServicePrincipalName** que coinciden con su SPN. Para obtener más información acerca de la búsqueda en el [catálogo global, vea Buscar en el catálogo global](searching-global-catalog-contents.md).

 

 




