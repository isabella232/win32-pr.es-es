---
description: Microsoft proporciona el paquete de autenticación MSV1 0 para los inicios de sesión de máquina \_ local que no requieren autenticación personalizada.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 Authentication Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173457"
---
# <a name="msv1_0-authentication-package"></a>Paquete de autenticación MSV1 \_ 0

Microsoft proporciona el paquete de autenticación MSV1 0 para los inicios de sesión de máquina \_ local que no requieren autenticación personalizada. [](../secgloss/a-gly.md) La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) llama al paquete de autenticación MSV1 0 para procesar los datos de inicio de sesión recopilados por la GINA para el proceso de inicio de sesión de \_ [*Winlogon.*](../secgloss/w-gly.md) [](../secgloss/g-gly.md) El paquete MSV1 0 comprueba la base de datos del administrador de cuentas de seguridad local (SAM) para determinar si los datos de inicio de sesión pertenecen a una entidad de seguridad válida y, a continuación, devuelve el resultado del intento de inicio de sesión al \_ LSA. [](../secgloss/s-gly.md)

MSV1 \_ 0 también admite inicios de sesión de dominio. MSV1 0 procesa los inicios de sesión de dominio mediante la autenticación de paso a través, como \_ se muestra en el diagrama siguiente.

![Paquete de autenticación msv1 \- 0](images/lsaint4.png)

En la autenticación de paso a través, la instancia local de MSV1 0 usa el servicio Netlogon para llamar a la instancia de \_ MSV1 0 que se ejecuta en el controlador \_ de dominio. A continuación, la instancia del controlador de dominio de MSV1 0 comprueba la base de datos SAM del controlador de dominio y devuelve el resultado del inicio de sesión a la instancia de \_ MSV1 0 en el \_ equipo local. La versión local de MSV1 0 reenvía el resultado de inicio de sesión a la instancia del \_ LSA en el equipo local.

Si el controlador de dominio no está disponible [](../secgloss/c-gly.md) y el LSA contiene credenciales almacenadas en caché para el usuario, la instancia local de MSV1 0 puede autenticar al usuario mediante los datos de inicio de sesión almacenados en \_ caché.

El paquete de autenticación MSV1 \_ 0 también admite [paquetes de subautentificación.](subauthentication-packages.md) Un paquete de subautentación es un archivo DLL que puede reemplazar parte de los criterios de autenticación y validación usados por el paquete de autenticación MSV1 \_ 0.

El paquete de autenticación MSV1 \_ 0 define un par [*clave-valor*](../secgloss/p-gly.md) de cadena de credenciales principales. La cadena de credenciales principales contiene las credenciales derivadas de los datos proporcionados en el momento del inicio de sesión. Incluye el nombre de usuario y las formas que distinguen mayúsculas de minúsculas y no distinguen mayúsculas de minúsculas de la contraseña del usuario.

 

 
