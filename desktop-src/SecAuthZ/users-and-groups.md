---
description: Explica la definición de usuarios y grupos en la API de Authorization Manager.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuarios y grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7d6ae84dba833ddd06eb81944cecb9aa401c0f8f1971c3164317cefae14fbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906825"
---
# <a name="users-and-groups"></a>Usuarios y grupos

En el Administrador de autorización, los destinatarios de la directiva de autorización se representan mediante los grupos siguientes:

-   Usuarios y grupos de Windows

    Estos grupos incluyen usuarios, equipos y grupos integrados para entidades de seguridad.

-   Grupos de consultas LDAP

    La pertenencia a estos grupos se calcula dinámicamente según sea necesario a partir de consultas del Protocolo ligero de acceso a directorios (LDAP). Un grupo de consulta LDAP es un tipo de grupo de aplicación.

-   Grupos de aplicaciones básicos

    Estos grupos constan de grupos de consultas LDAP, Windows usuarios y grupos, y otros grupos de aplicaciones básicos.

## <a name="windows-users-and-groups"></a>Usuarios y grupos de Windows

Son los mismos que los usuarios y grupos que se usan en Windows sistema operativo.

## <a name="ldap-query-groups"></a>Grupos de consultas LDAP

En el Administrador de autorización, puede usar consultas LDAP para hacer coincidir los atributos del usuario con los del objeto del usuario en Active Directory.

Por ejemplo, la consulta siguiente busca a todos excepto Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



La consulta siguiente busca todos los miembros del alias de alguien en www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grupos de aplicaciones básicos

En la API del Administrador de autorización, un grupo de aplicaciones se representa mediante un [**objeto IAzApplicationGroup.**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) Un grupo de aplicación básico es un tipo de grupo de aplicación.

Para definir la pertenencia básica al grupo de aplicaciones, defina quién es miembro y defina quién no es miembro. Ambos pasos se llevan a cabo de la misma manera. Especifique cero o más Windows usuarios y grupos, grupos de aplicaciones básicos definidos previamente o grupos de consultas LDAP. La pertenencia del grupo de aplicaciones básico se calcula quitando los miembros que no son miembros del grupo. El Administrador de autorización lo hace automáticamente en tiempo de ejecución.

La no pertenencia en un grupo de aplicaciones básico tiene prioridad sobre la pertenencia.

No se permiten definiciones de pertenencia circular; se produce el siguiente mensaje de error: "No se puede agregar GroupName. Se produjo el siguiente problema: se ha detectado un bucle ."

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



