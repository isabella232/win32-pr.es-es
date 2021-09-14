---
description: Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Protección de clientes y proveedores de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967132"
---
# <a name="securing-c-clients-and-providers"></a>Protección de clientes y proveedores de C++

Tanto los proveedores de C++ como las aplicaciones cliente deben realizar muchas de las mismas operaciones para mantener la seguridad de WMI.

Las aplicaciones cliente deben establecer correctamente los niveles de [suplantación y](setting-the-default-process-security-level-using-c-.md) [autenticación](setting-authentication-in-wmi.md) de DCOM al conectarse a WMI. Las devoluciones de [llamada](setting-security-on-an-asynchronous-call.md) de llamadas asincrónicas [](performing-access-checks.md) tienen riesgos de seguridad, por lo que las aplicaciones cliente deben realizar comprobaciones de acceso para asegurarse de que la devolución de llamada es de un origen de confianza. Los clientes necesitan proteger los [consumidores de eventos temporales y permanentes.](securing-wmi-events.md)

Un proveedor puede [realizar comprobaciones de acceso](performing-access-checks.md) para asegurarse de que solo los clientes adecuados acceden a los recursos que crea.

Tanto los proveedores como los clientes también pueden establecer la seguridad en una [conexión de proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) específica. Ambos también pueden habilitar [privilegios](executing-privileged-operations.md). Un proveedor de eventos debe asegurarse de que el consumidor cliente tiene privilegios para [recibir un evento solicitado.](providing-events-securely.md)

Es posible que un cliente o proveedor tenga que realizar una conexión remota que requiera un servicio de autenticación diferente, NTLM en lugar de Kerberos, por ejemplo.

 

 



