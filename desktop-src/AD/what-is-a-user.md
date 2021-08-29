---
title: Qué es un usuario
description: Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- ¿Qué es un usuario Active Directory
- usuarios Active Directory , qué es un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5647caef184b1e2b18e7639f1540afde013a3ba33ab58adbd402296656ca44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024422"
---
# <a name="what-is-a-user"></a>¿Qué es un usuario?

Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services. Los usuarios o programas humanos, como los servicios del sistema, pueden usar cuentas de usuario para iniciar sesión en un equipo. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándolo con los datos almacenados en el objeto de usuario del usuario en el Active Directory usuario. Si la contraseña se autentica, es decir, la contraseña presentada coincide con la contraseña almacenada en el objeto de usuario, el sistema genera un token de acceso. Un token de acceso es un objeto que describe el contexto de seguridad de un proceso o subproceso. Los datos de un token incluyen la identidad de seguridad y las pertenencias a grupos de la cuenta de usuario asociada al proceso o subproceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

Cada usuario o aplicación que accede a los recursos de un Windows dominio debe tener una cuenta en el Active Directory servidor. Windows esta cuenta de usuario para comprobar que el usuario o la aplicación tienen permiso para usar un recurso.

Se puede usar una cuenta de usuario para:

-   Permitir que los usuarios humanos inicien sesión en un equipo y accedan a los recursos en función de la identidad de esa cuenta de usuario.
-   Permitir que los programas y servicios se ejecuten en un contexto de seguridad específico.
-   Administre el acceso de los usuarios a recursos compartidos, como objetos y sus propiedades, recursos compartidos de red, archivos, directorios, colas de impresoras, entre otros.

Los grupos pueden contener miembros, que son referencias a usuarios y otros grupos. Los grupos también se pueden usar para controlar el acceso a los recursos compartidos. Al asignar permisos para recursos, por ejemplo, recursos compartidos de archivos, impresoras, entre otros, los administradores deben asignar esos permisos a un grupo en lugar de a los usuarios individuales. Los permisos se asignan una vez al grupo, en lugar de varias veces a cada usuario individual. Esto ayuda a simplificar el mantenimiento y la administración de una red.

## <a name="users-compared-to-contacts"></a>Usuarios comparados con contactos

Tanto los usuarios como los contactos se pueden usar para representar a usuarios humanos. Sin embargo, un usuario es una entidad de seguridad. un contacto no lo es.

Un usuario puede usarse para permitir que un usuario humano inicie sesión y acceda a recursos compartidos.

Un contacto solo se usa para la lista de distribución y el correo electrónico. Sin embargo, un contacto puede contener la mayoría de los datos almacenados en un objeto de usuario, como la dirección, los números de teléfono, entre otros, porque tanto el usuario como el contacto se derivan del objeto **classSchema** de la persona. Un contacto no tiene ningún contexto de seguridad; por lo tanto, no se puede usar un contacto para controlar el acceso a los recursos compartidos y no se puede usar para iniciar sesión en un equipo.

## <a name="users-compared-to-computers"></a>Usuarios comparados con equipos

La clase de objeto de equipo hereda de la clase de objeto de usuario. Un objeto de equipo representa un equipo; sin embargo, el equipo y los servicios locales del equipo a menudo requieren acceso a la red y a los recursos compartidos. Cuando el equipo accede a recursos compartidos, no al usuario que inició sesión en el equipo, necesita un token de acceso igual que un usuario humano que inició sesión como un usuario. Cuando un equipo accede a la red, usa un token de acceso que contiene el identificador de seguridad de la cuenta de equipo del equipo y los grupos que la cuenta es miembro.

Un servicio se puede ejecutar en el contexto de LocalSystem o en una cuenta de servicio específica. En equipos que Windows 2000, un servicio que se ejecuta en el contexto de la cuenta LocalSystem usa las credenciales del equipo.

 

 




