---
title: Proveedores de seguridad
description: La interfaz del proveedor de compatibilidad de seguridad (SSPI) proporciona compatibilidad con la autenticación mutua y se expone directamente a través de las API de SSPI y los servicios en capas en SSPI, incluido RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3685ad95b5e339853be947170bb0a8681a376d8d2f34368534d02b3b0cbdf4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183660"
---
# <a name="security-providers"></a>Proveedores de seguridad

La interfaz del proveedor de compatibilidad de seguridad (SSPI) proporciona compatibilidad con la autenticación mutua y se expone directamente a través de las API de SSPI y los servicios en capas en SSPI, incluido RPC.

No todos los paquetes de seguridad disponibles para SSPI admiten la autenticación mutua. Para obtener la autenticación mutua, la aplicación debe solicitar la autenticación mutua y un paquete de seguridad que la admita. Por ejemplo, el ejemplo de código de autenticación mutua en un servicio [de sockets](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) de Windows con un SCP usa el paquete "negotiate" en Secur32.dll, que se incluye con Windows 2000.

 

 




