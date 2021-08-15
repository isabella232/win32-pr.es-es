---
description: El Windows operativo admite la autenticación mediante paquetes de seguridad que funcionan como proveedores de soporte técnico de seguridad y como paquetes de autenticación.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Proveedores de compatibilidad de seguridad/paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918344"
---
# <a name="security-support-providerauthentication-packages"></a>Proveedores de compatibilidad de seguridad/paquetes de autenticación

El Windows operativo admite la [](../secgloss/s-gly.md) autenticación mediante paquetes de seguridad que funcionan como proveedores de soporte técnico de seguridad [*y*](../secgloss/s-gly.md) como paquetes [*de autenticación*](../secgloss/a-gly.md). Los paquetes de seguridad proporcionan los servicios de compatibilidad del proceso de inicio de sesión de un [](sspi.md) paquete de autenticación de Windows y también proporcionan servicios de autenticación a las aplicaciones mediante la implementación de un conjunto de funciones que están asignadas a la interfaz del proveedor de compatibilidad de seguridad (SSPI).

Un paquete de seguridad que funciona como paquete de autenticación e implementa la funcionalidad requerida por [*SSPI*](../secgloss/s-gly.md) se denomina proveedor de compatibilidad de seguridad/paquete de autenticación (SSP/AP).

Para obtener más información sobre los paquetes de seguridad, vea [Paquetes SSP proporcionados por Microsoft](ssp-packages-provided-by-microsoft.md). Para obtener información sobre el desarrollo de SSP/AP personalizados, vea [Paquetes de seguridad personalizados.](custom-security-packages.md)

 

 
