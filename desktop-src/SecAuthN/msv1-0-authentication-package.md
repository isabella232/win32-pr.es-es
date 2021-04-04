---
description: Microsoft proporciona el \_ paquete de autenticación MSV1 0 para los inicios de sesión del equipo local que no requieren autenticación personalizada.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 paquete de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278129"
---
# <a name="msv1_0-authentication-package"></a>Paquete de autenticación de MSV1 \_ 0

Microsoft proporciona el \_ paquete de [*autenticación*](../secgloss/a-gly.md) MSV1 0 para los inicios de sesión del equipo local que no requieren autenticación personalizada. La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) llama al \_ paquete de autenticación MSV1 0 para procesar los datos de inicio de sesión recopilados por [*Gina*](../secgloss/g-gly.md) para el proceso de inicio de sesión de [*Winlogon*](../secgloss/w-gly.md) . El \_ paquete MSV1 0 comprueba la base de datos del administrador de cuentas de seguridad (SAM) local para determinar si los datos de inicio de sesión pertenecen a una [*entidad de seguridad*](../secgloss/s-gly.md) válida y, a continuación, devuelve el resultado del intento de inicio de sesión a la LSA.

MSV1 \_ 0 también admite inicios de sesión de dominio. MSV1 \_ 0 procesa los inicios de sesión de dominio mediante la autenticación de paso a través, como se muestra en el diagrama siguiente.

![paquete de autenticación de msv1 \- 0](images/lsaint4.png)

En la autenticación de paso a través, la instancia local de MSV1 \_ 0 usa el servicio NetLogon para llamar a la instancia de MSV1 \_ 0 que se ejecuta en el controlador de dominio. La instancia del controlador de dominio de MSV1 \_ 0 comprueba entonces la base de datos SAM del controlador de dominio y devuelve el resultado de inicio de sesión a la instancia de MSV1 \_ 0 en el equipo local. La versión local de MSV1 \_ 0 reenvía el resultado de inicio de sesión a la instancia de LSA en el equipo local.

Si el controlador de dominio no está disponible y la LSA contiene [*credenciales*](../secgloss/c-gly.md) almacenadas en caché para el usuario, la instancia local de MSV1 \_ 0 puede autenticar al usuario mediante los datos de inicio de sesión almacenados en la memoria caché.

El \_ paquete de autenticación MSV1 0 también [admite paquetes](subauthentication-packages.md)de subautenticación. Un paquete de subautenticación es un archivo DLL que puede reemplazar parte de los criterios de autenticación y validación utilizados por el \_ paquete de autenticación MSV1 0.

El \_ paquete de autenticación MSV1 0 define un par clave/valor de cadena de [*credenciales principales*](../secgloss/p-gly.md) . La cadena de credenciales principal contiene las credenciales derivadas de los datos proporcionados en la hora de inicio de sesión. Incluye el nombre de usuario y las formas con distinción de mayúsculas y minúsculas y sin distinción de mayúsculas y minúsculas de la contraseña del usuario.

 

 
