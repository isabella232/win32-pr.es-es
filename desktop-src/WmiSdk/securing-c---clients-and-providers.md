---
description: Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protección de clientes y proveedores de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706086"
---
# <a name="securing-c-clients-and-providers"></a>Protección de clientes y proveedores de C++

Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.

Las aplicaciones cliente deben establecer los niveles de [suplantación](setting-the-default-process-security-level-using-c-.md) y [autenticación](setting-authentication-in-wmi.md) de DCOM correctamente al conectarse a WMI. Las devoluciones de llamada de [llamadas asincrónicas](setting-security-on-an-asynchronous-call.md) tienen riesgos de seguridad, por lo que las aplicaciones cliente deben [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que la devolución de llamada proviene de un origen de confianza. Los clientes necesitan proteger a los [consumidores de eventos temporales y permanentes](securing-wmi-events.md).

Un proveedor puede [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que los clientes adecuados solo tienen acceso a los recursos que crea.

Tanto los proveedores como los clientes también pueden establecer la seguridad en una conexión de [proxy específica](setting-the-security-on-iwbemservices-and-other-proxies.md) . Ambos también pueden habilitar los [privilegios](executing-privileged-operations.md). Un proveedor de eventos debe asegurarse de que el consumidor del cliente tenga privilegios para [recibir un evento solicitado](providing-events-securely.md).

Es posible que un cliente o un proveedor necesiten realizar una conexión remota que requiera un servicio de autenticación diferente, NTLM en lugar de Kerberos, por ejemplo.

 

 



