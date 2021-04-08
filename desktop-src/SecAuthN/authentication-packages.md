---
description: Los paquetes de autenticación se encuentran en bibliotecas de vínculos dinámicos.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff02017b653521d80741bcdf3c205ab924c4bceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910638"
---
# <a name="authentication-packages"></a>Paquetes de autenticación

Los [*paquetes de autenticación*](/windows/desktop/SecGloss/a-gly) se encuentran en bibliotecas de vínculos dinámicos. La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) carga los paquetes de autenticación mediante la información de configuración almacenada en el registro. La carga de varios paquetes de autenticación permite que LSA admita varios procesos de inicio de sesión y varios [*protocolos de seguridad*](/windows/desktop/SecGloss/s-gly).

Los procesos de inicio de sesión usan paquetes de autenticación para analizar los datos de inicio de sesión. Los nuevos procesos de inicio de sesión se agregan a un sistema agregando un [*Gina*](/windows/desktop/SecGloss/g-gly) para recopilar los datos de inicio de sesión necesarios y, si es necesario, agregando un nuevo paquete de autenticación para analizar los datos.

Los paquetes de autenticación implementan los protocolos de seguridad. Un paquete de autenticación analiza los datos de inicio de sesión siguiendo las reglas y los procedimientos establecidos en un protocolo de seguridad.

Los paquetes de autenticación son responsables de las siguientes tareas:

-   Análisis de los datos de inicio de sesión para determinar si una [*entidad de seguridad*](/windows/desktop/SecGloss/s-gly) puede iniciar sesión en un sistema.
-   Establecer una nueva [*sesión de inicio*](/windows/desktop/SecGloss/l-gly) de sesión y crear un [*identificador de inicio de sesión*](/windows/desktop/SecGloss/l-gly) único para la entidad de seguridad autenticada correctamente.
-   Pasar información de seguridad a LSA para el token de seguridad de la entidad de seguridad.

Cuando un usuario intenta realizar un inicio de sesión interactivo, LSA llama a un paquete de autenticación para determinar si se permite que el usuario inicie sesión. MSV1 \_ 0, por ejemplo, es un paquete de autenticación instalado con el sistema operativo Microsoft Windows. El \_ paquete MSV1 0 acepta un nombre de usuario y una contraseña con [*hash*](/windows/desktop/SecGloss/h-gly) . Busca la combinación de nombre de usuario y contraseña con hash en la base de datos del administrador de cuentas de seguridad (SAM). Si los datos de inicio de sesión coinciden con las [*credenciales*](/windows/desktop/SecGloss/c-gly)almacenadas, el paquete de autenticación permite que el inicio de sesión se realice correctamente.

Después de autenticar correctamente las credenciales [*de una entidad de seguridad*](/windows/desktop/SecGloss/s-gly) , un paquete de autenticación es responsable de crear una nueva sesión de inicio de sesión de LSA para la entidad de seguridad y de asignar el identificador de inicio de [*sesión*](/windows/desktop/SecGloss/l-gly) que identifica de forma única la sesión de inicio de sesión. El paquete de autenticación puede asociar la información de credenciales con la sesión de inicio de sesión para las solicitudes de autenticación posteriores. Por ejemplo, el \_ paquete de autenticación MSV1 0 (proporcionado por Microsoft) asocia el nombre de la cuenta de usuario y un hash de la contraseña del usuario con cada sesión de inicio de sesión.

El paquete de autenticación también proporciona un conjunto de [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) y otra información adecuada para su inclusión en el token de seguridad creado por la LSA. Este token representa el [*contexto*](/windows/desktop/SecGloss/c-gly) de seguridad de la entidad de seguridad para el acceso a las operaciones de Windows.

Después de crear una sesión de inicio de sesión y asociarla a una entidad de seguridad, las solicitudes de autenticación posteriores realizadas en nombre de la entidad de seguridad se administran de forma diferente que el inicio de sesión inicial. El paquete de autenticación no crea una nueva sesión de inicio de sesión ni devuelve información para crear un token. El paquete de autenticación puede, sin embargo, asociar [*las credenciales complementarias*](/windows/desktop/SecGloss/s-gly) obtenidas durante una autenticación posterior con la sesión de inicio de sesión existente de la entidad de seguridad. Las credenciales adicionales se obtienen cuando el acceso a un recurso solicitado requiere información más allá de las credenciales establecidas por el inicio de sesión inicial. Por ejemplo, cuando un usuario que ha iniciado la sesión solicita un inicio de sesión de red de Novell, se puede llamar a un paquete de autenticación específico de Novell y se pueden autenticar y asociar las credenciales específicas de Novell con la sesión de inicio de sesión. Un redirector de Novell puede hacer referencia a estas credenciales (mediante el paquete de autenticación de Novell) cuando el usuario accede a la red de Novell.

En los temas siguientes se tratan los distintos tipos de [*paquetes de autenticación*](/windows/desktop/SecGloss/a-gly):

-   [Paquetes de autenticación de Windows](windows-authentication-packages.md)
-   [Paquetes de autenticación/proveedor de compatibilidad de seguridad](security-support-provider-authentication-packages.md)
-   [Paquetes de autenticación proporcionados por Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Paquetes de subautenticación](subauthentication-packages.md)

 

 
