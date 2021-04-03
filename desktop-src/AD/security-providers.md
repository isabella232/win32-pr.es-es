---
title: Proveedores de seguridad
description: La interfaz del proveedor de compatibilidad para seguridad (SSPI) proporciona compatibilidad con la autenticación mutua y se expone directamente a través de las API y servicios de SSPI superpuestos en SSPI, incluido RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075102"
---
# <a name="security-providers"></a>Proveedores de seguridad

La interfaz del proveedor de compatibilidad para seguridad (SSPI) proporciona compatibilidad con la autenticación mutua y se expone directamente a través de las API y servicios de SSPI superpuestos en SSPI, incluido RPC.

No todos los paquetes de seguridad disponibles para SSPI admiten la autenticación mutua. Para obtener la autenticación mutua, la aplicación debe solicitar la autenticación mutua y un paquete de seguridad que la admita. Por ejemplo, el ejemplo de código de la [autenticación mutua en un servicio de Windows Sockets con un SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) usa el paquete "Negotiate" en Secur32.dll, que se incluye con Windows 2000.

 

 




