---
description: Explica las diferencias entre SSP/AP y SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/AP frente a SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c471e529a478cadbfcc385a1b0d699a4539e7bc80beeb2d40e01e2f7e9f428d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917271"
---
# <a name="sspaps-vs-ssps"></a>SSP/AP frente a SSP

[*Los paquetes*](../secgloss/s-gly.md) de seguridad se implementan en uno de los siguientes tipos de bibliotecas de vínculos dinámicos (DLL):

-   [SSP/AP](#sspaps-vs-ssps)
-   [Ssps](#sspaps-vs-ssps)

Si un paquete de seguridad se [](../secgloss/a-gly.md) encuentra en un proveedor de compatibilidad de seguridad o un paquete de autenticación (SSP/AP) o en un archivo DLL de proveedor de soporte técnico de seguridad (SSP), viene determinado por los tipos de servicios de seguridad que proporciona y la medida en que requiere la integración con la autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA). [](../secgloss/s-gly.md) Estas diferencias también determinan la API implementada en un paquete de seguridad personalizado.

## <a name="sspaps"></a>SSP/AP

Un SSP/AP es un archivo [](../secgloss/s-gly.md) DLL que contiene uno o varios paquetes de seguridad [](authentication-packages.md) y puede funcionar como un SSP para aplicaciones cliente/servidor y como un paquete de autenticación para aplicaciones de inicio de sesión. Para funcionar en ambos roles, los SSP/AP se cargan en el espacio de procesos LSA durante el inicio del sistema y también se pueden cargar en procesos de aplicación cliente/servidor.

Los paquetes de seguridad SSP/AP personalizados deben implementar las funciones implementadas por [SSP/AP](authentication-functions.md)en modo de usuario y las funciones implementadas por [SSP/AP.](authentication-functions.md) Estas implementaciones de función pueden hacer uso de las funciones de compatibilidad de LSA para ofrecer características de seguridad avanzadas, como la creación de [*tokens,*](../secgloss/s-gly.md) la compatibilidad con credenciales complementarias y la autenticación de paso a través.

Si un paquete de seguridad SSP/AP [](../secgloss/i-gly.md) personalizado proporciona toda la gama de funciones de privacidad y integridad de mensajes, también implementará las funciones implementadas por [SSP/AP en](authentication-functions.md)modo de usuario.

## <a name="ssps"></a>Ssps

Un SSP es un archivo DLL que contiene uno o varios paquetes de seguridad que proporcionan servicios autenticados de conexión, integridad de mensajes y cifrado de mensajes a las aplicaciones cliente/servidor. Los SSP implementan [funciones de interfaz](sspi.md) de proveedor de compatibilidad de seguridad (SSPI). Las aplicaciones pueden acceder a los paquetes de seguridad de un SSP llamando directamente a las funciones de SSPI. Los SSP se cargan en los procesos de cliente y servidor; no están integradas con el LSA.

 

 
