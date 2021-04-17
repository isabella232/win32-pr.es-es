---
description: Explica la definición de usuarios y grupos en la API de administrador de autorización.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuarios y grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653069"
---
# <a name="users-and-groups"></a>Usuarios y grupos

En Administrador de autorización, los destinatarios de la Directiva de autorización se representan mediante los siguientes grupos:

-   Usuarios y grupos de Windows

    Estos grupos incluyen usuarios, equipos y grupos integrados para entidades de seguridad.

-   Grupos de consulta LDAP

    La pertenencia a estos grupos se calcula dinámicamente según sea necesario desde las consultas de Protocolo ligero de acceso a directorios (LDAP). Un grupo de consulta LDAP es un tipo de grupo de aplicación.

-   Grupos de aplicaciones básicos

    Estos grupos se componen de grupos de consulta LDAP, usuarios y grupos de Windows y otros grupos de aplicaciones básicos.

## <a name="windows-users-and-groups"></a>Usuarios y grupos de Windows

Son los mismos que los usuarios y grupos que se usan en todo el sistema operativo Windows.

## <a name="ldap-query-groups"></a>Grupos de consulta LDAP

En Administrador de autorización, puede usar consultas LDAP para hacer coincidir los atributos del usuario con los del objeto del usuario en Active Directory.

Por ejemplo, la siguiente consulta busca todos los usuarios excepto Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



La siguiente consulta busca todos los miembros del alias alguien en www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grupos de aplicaciones básicos

En la API de administrador de autorización, un grupo de aplicaciones se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) . Un grupo de aplicación básico es un tipo de grupo de aplicación.

Para definir la pertenencia a grupos de aplicaciones básica, defina quién es miembro y defina quién no es miembro. Ambos pasos se realizan de la misma manera. Especifique cero o más usuarios y grupos de Windows, grupos de aplicaciones básicos definidos previamente o grupos de consultas LDAP. La pertenencia del grupo de aplicación básico se calcula quitando los miembros del grupo. Administrador de autorización lo hace automáticamente en tiempo de ejecución.

La no afiliación de un grupo de aplicación básico tiene prioridad sobre la pertenencia.

No se permiten definiciones de pertenencia circulares; dan como resultado el siguiente mensaje de error: "no se puede Agregar GroupName. Se produjo el siguiente problema: se ha detectado un bucle ".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



