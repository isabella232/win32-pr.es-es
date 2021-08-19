---
description: Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protección de clientes y proveedores de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4151440f9e85f7cd9e6590842ffd3d103242410b38f52287dba83ba3bb3faec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316164"
---
# <a name="securing-c-clients-and-providers"></a>Protección de clientes y proveedores de C++

Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.

Las aplicaciones cliente deben establecer correctamente los niveles de [suplantación y](setting-the-default-process-security-level-using-c-.md) [autenticación de](setting-authentication-in-wmi.md) DCOM al conectarse a WMI. Las devoluciones de llamada de [llamadas asincrónicas](setting-security-on-an-asynchronous-call.md) [](performing-access-checks.md) tienen riesgos de seguridad, por lo que las aplicaciones cliente deben realizar comprobaciones de acceso para asegurarse de que la devolución de llamada es de un origen de confianza. Los clientes necesitan proteger los consumidores de eventos temporales [y permanentes.](securing-wmi-events.md)

Un proveedor puede [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que solo los clientes adecuados acceden a los recursos que crea.

Tanto los proveedores como los clientes también pueden establecer la seguridad en una [conexión de proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) específica. Ambos también pueden habilitar [privilegios](executing-privileged-operations.md). Un proveedor de eventos debe asegurarse de que el consumidor cliente tiene privilegios para [recibir un evento solicitado.](providing-events-securely.md)

Es posible que un cliente o proveedor tenga que realizar una conexión remota que requiera un servicio de autenticación diferente, NTLM en lugar de Kerberos, por ejemplo.

 

 



