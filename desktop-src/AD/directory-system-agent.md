---
title: Agente de sistema de directorio
description: El agente de sistema de directorio (DSA) es una colección de servicios y procesos que se ejecutan en cada controlador de dominio y proporciona acceso al almacén de datos.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Active Directory del agente de sistema de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904505"
---
# <a name="directory-system-agent"></a>Agente de sistema de directorio

El [*agente de sistema de directorio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) es una colección de servicios y procesos que se ejecutan en cada controlador de dominio y proporciona acceso al almacén de datos. El almacén de datos es el almacenamiento físico de los datos de directorio ubicados en un disco duro. En Active Directory Domain Services, el DSA es parte del subsistema de la entidad de sistema local (LSA). Los clientes acceden al directorio mediante uno de los siguientes mecanismos admitidos por el DSA:

-   Los clientes LDAP se conectan al DSA mediante el Protocolo ligero de acceso a directorios (LDAP). Active Directory Domain Services admite LDAP 3,0, definido por RFC 3377 y LDAP 2,0, definido por RFC 1777. Los clientes de Windows usan LDAP 3,0 para conectarse al DSA.
-   Los clientes MAPI, como Microsoft Exchange Server, se conectan al DSA mediante la interfaz de llamada a procedimiento remoto de MAPI.
-   Los DSA en Active Directory Domain Services conectarse entre sí para realizar la replicación mediante una interfaz de llamada a procedimiento remoto propia.

 

 