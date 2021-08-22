---
description: Explica el modelo de autenticación LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modelo de autenticación LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762595332252c22141aebdc7f3ecbe168e49a83795830a0cb03e49eb5da73ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140948"
---
# <a name="lsa-authentication-model"></a>Modelo de autenticación LSA

El [*modelo de autenticación de*](../secgloss/l-gly.md) autoridad de seguridad local (LSA) tiene las siguientes características:

-   La autenticación LSA admite paquetes [de autenticación personalizados.](authentication-packages.md) Esto permite a los clientes finales y a los proveedores de software independientes (ISV) personalizar o reemplazar las rutinas de autenticación para cumplir los requisitos más allá de los proporcionados por los paquetes de autenticación estándar de Microsoft. Aunque los paquetes de autenticación proporcionados por Microsoft requieren un nombre de usuario y datos de inicio de sesión de contraseña, un paquete de autenticación personalizado puede tomar otras formas de datos de inicio de sesión, como la información de la tarjeta ATM y un número de identificación personal (PIN). También se puede usar un paquete de autenticación personalizado para implementar un nuevo protocolo [*de seguridad*](../secgloss/s-gly.md).
-   LSA admite paquetes de seguridad personalizados, que funcionan como proveedores de compatibilidad de seguridad para aplicaciones distribuidas y como paquetes de autenticación para aplicaciones que requieren servicios de autenticación. Se accede a la funcionalidad de autenticación mediante la misma interfaz que un paquete [](sspi.md) de autenticación independiente, mientras que a la funcionalidad del proveedor de compatibilidad de seguridad se accede mediante la interfaz del proveedor de soporte técnico de seguridad (SSPI). El conjunto de funciones de compatibilidad de LSA disponibles para los paquetes de seguridad personalizados les permite proporcionar características de seguridad avanzadas, como la creación de tokens y la [*administración complementaria de credenciales.*](../secgloss/s-gly.md)
-   LSA admite la administración de credenciales heterogéneo para la interfaz con productos que no son de Microsoft, como redes y bases de datos. Dado que estos productos a menudo tienen sus propias credenciales de seguridad, el LSA proporciona funciones que los paquetes de autenticación pueden usar para asociar credenciales que no son de Microsoft con Windows procesos. Los paquetes de autenticación personalizados pueden proporcionar servicios para consultar estas credenciales cuando sea necesario, como cuando un redirector de red intenta establecer una conexión a un sistema remoto.
-   Cada clase de dispositivo de inicio de sesión instalado en un sistema puede tener su propio proceso de inicio de sesión. Las clases de dispositivo suelen incluir dispositivos como lectores de tarjetas inteligentes. sin embargo, para los fines de la autenticación [*LSA,*](../secgloss/l-gly.md) las redes conectadas también se tratan como dispositivos. De forma predeterminada, el Windows operativo proporciona el proceso de inicio de sesión que admite inicios de sesión de nombre de usuario y contraseña mediante un teclado. Los desarrolladores pueden agregar compatibilidad con otros dispositivos, como [*lectores de tarjetas*](../secgloss/s-gly.md) [*inteligentes.*](../secgloss/r-gly.md) Para obtener más información sobre las tarjetas inteligentes, vea [Autenticación con tarjeta inteligente.](smart-card-authentication.md) Para obtener más información sobre la compatibilidad con dispositivos de inicio de sesión, [consulte Winlogon y GINA.](winlogon-and-gina.md)

 

 
