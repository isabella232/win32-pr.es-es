---
description: El sistema operativo Windows admite la autenticación mediante paquetes de seguridad que funcionan como proveedores de compatibilidad de seguridad y como paquetes de autenticación.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Paquetes de autenticación/proveedor de compatibilidad de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648367"
---
# <a name="security-support-providerauthentication-packages"></a>Paquetes de autenticación/proveedor de compatibilidad de seguridad

El sistema operativo Windows admite la autenticación mediante [*paquetes de seguridad*](../secgloss/s-gly.md) que funcionan como proveedores de compatibilidad de [*seguridad*](../secgloss/s-gly.md) y como paquetes de [*autenticación*](../secgloss/a-gly.md). Los paquetes de seguridad proporcionan los servicios de soporte del proceso de inicio de sesión de un paquete de autenticación de Windows y también proporcionan servicios de autenticación a las aplicaciones implementando un conjunto de funciones que se asignan a la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI).

Un paquete de seguridad que funciona como un paquete de autenticación e implementa la funcionalidad requerida por [*SSPI*](../secgloss/s-gly.md) se denomina proveedor de compatibilidad para seguridad/paquete de autenticación (SSP/AP).

Para obtener más información acerca de los paquetes de seguridad, consulte [paquetes SSP proporcionados por Microsoft](ssp-packages-provided-by-microsoft.md). Para obtener información sobre el desarrollo de SSP o AP personalizados, consulte [paquetes de seguridad personalizados](custom-security-packages.md).

 

 
