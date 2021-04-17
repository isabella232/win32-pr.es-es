---
description: Explica el modelo de autenticación LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modelo de autenticación LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f5a44a20284a7285eb7fcffe1d1f8f6bf1f286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652913"
---
# <a name="lsa-authentication-model"></a>Modelo de autenticación LSA

El modelo de autenticación de la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) tiene las siguientes características:

-   La autenticación LSA admite [paquetes de autenticación](authentication-packages.md)personalizados. Esto permite a los clientes finales y a los fabricantes de software independientes (ISV) personalizar o reemplazar las rutinas de autenticación para cumplir los requisitos más allá de los proporcionados por los paquetes de autenticación estándar de Microsoft. Aunque los paquetes de autenticación proporcionados por Microsoft requieren un nombre de usuario y los datos de inicio de sesión de contraseña, un paquete de autenticación personalizado puede tomar otras formas de datos de inicio de sesión, como la información de la tarjeta ATM y un número de identificación personal (PIN). También se puede usar un paquete de autenticación personalizado para implementar un nuevo [*Protocolo de seguridad*](../secgloss/s-gly.md).
-   LSA admite paquetes de seguridad personalizados, que funcionan como proveedores de compatibilidad de seguridad para aplicaciones distribuidas y como paquetes de autenticación para aplicaciones que requieren servicios de autenticación. Se tiene acceso a la funcionalidad de autenticación mediante la misma interfaz que un paquete de autenticación independiente, mientras que se tiene acceso a la funcionalidad del proveedor de compatibilidad para seguridad mediante la [interfaz del proveedor de compatibilidad para](sspi.md) seguridad (SSPI). El conjunto de funciones de compatibilidad de LSA disponibles para los paquetes de seguridad personalizados les permite proporcionar características de seguridad avanzadas, como la creación de tokens y la administración de [*credenciales adicionales*](../secgloss/s-gly.md) .
-   LSA admite la administración de credenciales heterogéneas para interactuar con productos que no son de Microsoft, como redes y bases de datos. Dado que estos productos suelen tener sus propias credenciales de seguridad, la LSA proporciona funciones que los paquetes de autenticación pueden utilizar para asociar las credenciales que no son de Microsoft con los procesos de Windows. Los paquetes de autenticación personalizados pueden proporcionar servicios para consultar estas credenciales cuando sea necesario, por ejemplo, cuando un redirector de red intenta establecer una conexión con un sistema remoto.
-   Cada clase de dispositivo de inicio de sesión instalado en un sistema puede tener su propio proceso de inicio de sesión. Las clases de dispositivo suelen incluir dispositivos como lectores de tarjetas inteligentes; sin embargo, para los fines de la autenticación [*LSA*](../secgloss/l-gly.md) , las redes conectadas también se tratan como dispositivos. De forma predeterminada, el sistema operativo Windows proporciona el proceso de inicio de sesión que admite inicios de sesión con nombre de usuario y contraseña mediante un teclado. Los desarrolladores pueden agregar compatibilidad con otros dispositivos, como [*lectores*](../secgloss/r-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) . Para obtener más información acerca de las tarjetas inteligentes, consulte [autenticación mediante tarjeta inteligente](smart-card-authentication.md). Para obtener más información acerca de la compatibilidad con dispositivos de inicio de sesión, consulte [Winlogon y Gina](winlogon-and-gina.md).

 

 
