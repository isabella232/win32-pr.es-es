---
title: Cómo un servicio crea sus SPN
description: Un servicio puede usar dos funciones para componer sus SPN DsGetSpn es una función de uso general para crear SPN y DsServerRegisterSpn es una función especializada para crear y registrar SPN simples para un servicio basado en host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nombre de entidad de seguridad de servicio ad , cómo se compone un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb659eec3bb2d0f50fd109b39f356df1429535
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881400"
---
# <a name="how-a-service-composes-its-spns"></a>Cómo un servicio crea sus SPN

Un servicio puede usar dos funciones para componer sus SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) es una función de uso general para crear SPN y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) es una función especializada para crear y registrar SPN simples para un servicio basado en host.

Normalmente, un instalador de servicio usa la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear SPN, que luego registra en la cuenta de inicio de sesión del servicio mediante la función [**DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) **DsGetSpn** puede realizar las siguientes funciones.

-   Cree un SPN simple con el formato <service class> / &lt; &gt; "host" para un servicio basado en host.
-   Cree un SPN complejo que incluya el componente "nombre de servicio" que usan los servicios replicables o el componente "puerto" que distingue varias instancias de un servicio en &lt; &gt; un único &lt; &gt; host.
-   Cree un único SPN con el componente " host " establecido en el nombre de un host especificado o en el nombre &lt; del equipo local de forma &gt; predeterminada.
-   Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en varios hosts en todo el bosque. Cada SPN especifica el nombre del host para una instancia de servicio.
-   Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en el mismo host. Cada SPN especifica el nombre del host y un número de puerto para una instancia de servicio.

La matriz de nombres devuelta por [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) debe liberarse llamando a la [**función DsFreeSpnArray.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)

Tenga en cuenta que las funciones [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) no comprueban que los SPN sean únicos. Dado que se produce un error en la autenticación mutua si un cliente presenta un SPN que no es único, compruebe la unidad antes de registrar un SPN. Para ello, busque en el catálogo global (GC) atributos **servicePrincipalName** que coincidan con el SPN. Para obtener más información sobre cómo buscar en gc, vea [Buscar en el catálogo global.](searching-global-catalog-contents.md)

 

 




