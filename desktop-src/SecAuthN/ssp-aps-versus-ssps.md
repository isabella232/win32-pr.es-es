---
description: Explica las diferencias entre SSP/APs y SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs frente a SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002599"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs frente a SSP

Los [*paquetes de seguridad*](../secgloss/s-gly.md) se implementan en uno de los siguientes tipos de bibliotecas de vínculos dinámicos (dll):

-   [SSP/APs](#sspaps-vs-ssps)
-   [SSP](#sspaps-vs-ssps)

El hecho de que un paquete de seguridad esté en un proveedor de soporte técnico de seguridad/[*paquete de autenticación*](../secgloss/a-gly.md) (SSP/AP) o un archivo dll de proveedor de [*compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) esté determinado por los tipos de servicios de seguridad que proporciona y por la medida en la que se requiere la integración con la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA). Estas diferencias también determinan la API implementada en un paquete de seguridad personalizado.

## <a name="sspaps"></a>SSP/APs

Un SSP/AP es un archivo DLL que contiene uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md) y puede funcionar como SSP para aplicaciones cliente/servidor y como un paquete de [autenticación](authentication-packages.md) para aplicaciones de inicio de sesión. Para funcionar en ambos roles, SSP/APs se cargan en el espacio de proceso de LSA al iniciar el sistema y se pueden cargar también en procesos de aplicación cliente/servidor.

Los paquetes de seguridad SSP/AP personalizados deben implementar las [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md)y [las funciones implementadas por SSP/APS](authentication-functions.md). Estas implementaciones de función pueden hacer uso de las funciones de compatibilidad de LSA para ofrecer características de seguridad avanzadas, como la creación de tokens, la compatibilidad con [*credenciales adicionales*](../secgloss/s-gly.md) y la autenticación de paso a través.

Si un paquete de seguridad SSP/AP personalizado proporciona toda la gama de funciones de [*integridad*](../secgloss/i-gly.md) y privacidad de los mensajes, también implementará las [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md).

## <a name="ssps"></a>SSP

Un SSP es un archivo DLL que contiene uno o varios paquetes de seguridad que proporcionan servicios de autenticación, integridad de mensajes y cifrado de mensajes a las aplicaciones cliente/servidor. Los SSP implementan funciones de la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI). Las aplicaciones pueden tener acceso a los paquetes de seguridad de un SSP llamando directamente a las funciones SSPI. Los SSP se cargan en los procesos de cliente y servidor; no están integradas con la LSA.

 

 
