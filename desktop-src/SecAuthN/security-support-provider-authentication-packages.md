---
description: El Windows operativo admite la autenticación mediante paquetes de seguridad que funcionan como proveedores de soporte técnico de seguridad y como paquetes de autenticación.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Proveedores de compatibilidad de seguridad/paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476547"
---
# <a name="security-support-providerauthentication-packages"></a>Proveedores de compatibilidad de seguridad/paquetes de autenticación

El Windows operativo admite la [](../secgloss/s-gly.md) autenticación mediante paquetes de seguridad que funcionan como proveedores de soporte técnico de seguridad [*y*](../secgloss/s-gly.md) como paquetes [*de autenticación*](../secgloss/a-gly.md). Los paquetes de seguridad proporcionan los servicios de compatibilidad del proceso de inicio de sesión de un paquete [](sspi.md) de autenticación de Windows y también proporcionan servicios de autenticación a las aplicaciones mediante la implementación de un conjunto de funciones que están asignadas a la interfaz del proveedor de compatibilidad de seguridad (SSPI).

Un paquete de seguridad que funciona como paquete de autenticación e implementa la funcionalidad requerida por [*SSPI*](../secgloss/s-gly.md) se denomina proveedor de compatibilidad de seguridad/paquete de autenticación (SSP/AP).

Para obtener más información sobre los paquetes de seguridad, vea [Paquetes SSP proporcionados por Microsoft](ssp-packages-provided-by-microsoft.md). Para obtener información sobre el desarrollo de SSP/AP personalizados, vea [Paquetes de seguridad personalizados.](custom-security-packages.md)

 

 
