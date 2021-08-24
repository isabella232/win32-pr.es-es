---
description: Los paquetes de autenticación se encuentran en bibliotecas de vínculos dinámicos.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141369"
---
# <a name="authentication-packages"></a>Paquetes de autenticación

[*Los paquetes de*](/windows/desktop/SecGloss/a-gly) autenticación se encuentran en bibliotecas de vínculos dinámicos. La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) carga los paquetes de autenticación mediante la información de configuración almacenada en el registro. La carga de varios paquetes de autenticación permite que el LSA admita varios procesos de inicio de sesión y varios [*protocolos de seguridad*](/windows/desktop/SecGloss/s-gly).

Los procesos de inicio de sesión usan paquetes de autenticación para analizar los datos de inicio de sesión. Los nuevos procesos de inicio de sesión se agregan a un sistema agregando un [*GINA*](/windows/desktop/SecGloss/g-gly) para recopilar los datos de inicio de sesión necesarios y, si es necesario, agregando un nuevo paquete de autenticación para analizar los datos.

Los protocolos de seguridad se implementan mediante paquetes de autenticación. Un paquete de autenticación analiza los datos de inicio de sesión siguiendo las reglas y los procedimientos establecidos en un protocolo de seguridad.

Los paquetes de autenticación son responsables de las siguientes tareas:

-   Analizar los datos de inicio de sesión para determinar si una [*entidad de seguridad*](/windows/desktop/SecGloss/s-gly) puede iniciar sesión en un sistema.
-   Establecer una nueva sesión [*de inicio de sesión*](/windows/desktop/SecGloss/l-gly) y crear un identificador de inicio de sesión [*único*](/windows/desktop/SecGloss/l-gly) para la entidad de seguridad autenticada correctamente.
-   Pasar información de seguridad al LSA para el token de seguridad de la entidad de seguridad.

Cuando un usuario intenta un inicio de sesión interactivo, el LSA llama a un paquete de autenticación para determinar si se permite al usuario iniciar sesión. MSV1 0, por ejemplo, es un paquete de autenticación instalado con microsoft \_ Windows sistema operativo. El paquete MSV1 \_ 0 acepta un nombre de usuario y una [*contraseña con*](/windows/desktop/SecGloss/h-gly) hash. Busca la combinación de nombre de usuario y contraseña con hash en la base de datos del Administrador de cuentas de seguridad (SAM). Si los datos de inicio de sesión coinciden con las [*credenciales almacenadas,*](/windows/desktop/SecGloss/c-gly)el paquete de autenticación permite que el inicio de sesión se realiza correctamente.

Después de autenticar [](/windows/desktop/SecGloss/s-gly) correctamente las credenciales de una entidad de seguridad, un paquete de autenticación [](/windows/desktop/SecGloss/l-gly) es responsable de crear una nueva sesión de inicio de sesión de LSA para la entidad de seguridad y de asignar el identificador de inicio de sesión que identifica de forma única la sesión de inicio de sesión. El paquete de autenticación puede asociar información de credenciales a la sesión de inicio de sesión para solicitudes de autenticación posteriores. Por ejemplo, el paquete de autenticación MSV1 0 (proporcionado por Microsoft) asocia el nombre de la cuenta de usuario y un hash de la contraseña del usuario con cada sesión \_ de inicio de sesión.

El paquete de autenticación [](/windows/desktop/SecGloss/s-gly) también proporciona un conjunto de identificadores de seguridad (SID) y otra información adecuada para su inclusión en el token de seguridad creado por el LSA. Este token representará el contexto de seguridad de la [*entidad de seguridad*](/windows/desktop/SecGloss/c-gly) para el acceso a Windows operaciones.

Una vez creada una sesión de inicio de sesión y asociada a una entidad de seguridad, las solicitudes de autenticación posteriores realizadas en nombre de la entidad de seguridad se controlan de forma diferente a la del inicio de sesión inicial. El paquete de autenticación no crea una nueva sesión de inicio de sesión ni devuelve información para crear un token. Sin embargo, el paquete de autenticación puede asociar las [*credenciales*](/windows/desktop/SecGloss/s-gly) complementarias obtenidas durante una autenticación posterior con la sesión de inicio de sesión existente de la entidad de seguridad. Las credenciales complementarias se obtienen cuando el acceso a un recurso solicitado requiere información más allá de las credenciales establecidas por el inicio de sesión inicial. Por ejemplo, cuando un usuario que ha iniciado sesión solicita un inicio de sesión de red de Telnet, se puede llamar a un paquete de autenticación específico de Kerberos y se pueden autenticar las credenciales específicas de Telnet y asociarse a la sesión de inicio de sesión. Un redirector de Icmp puede hacer referencia a estas credenciales (mediante el paquete de autenticación de Kerberos) cuando el usuario accede a la red de Kerberos.

En los temas siguientes se tratan los distintos tipos de [*paquetes de autenticación*](/windows/desktop/SecGloss/a-gly):

-   [Windows Paquetes de autenticación](windows-authentication-packages.md)
-   [Proveedores de compatibilidad de seguridad/paquetes de autenticación](security-support-provider-authentication-packages.md)
-   [Paquetes de autenticación proporcionados por Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Paquetes de subauauticación](subauthentication-packages.md)

 

 
