---
title: ¿Qué es un usuario?
description: Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- Qué es un usuario Active Directory
- usuarios Active Directory, qué es un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c59b2ea46474860268f327bcd03d2ba67ecea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773039"
---
# <a name="what-is-a-user"></a>¿Qué es un usuario?

Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services. Los usuarios o programas humanos, como los servicios del sistema, usan para iniciar sesión en un equipo. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándola con los datos almacenados en el objeto de usuario del usuario en el servidor de Active Directory. Si la contraseña se autentica, es decir, la contraseña presentada coincide con la contraseña almacenada en el objeto de usuario, el sistema genera un token de acceso. Un token de acceso es un objeto que describe el contexto de seguridad de un proceso o subproceso. Los datos de un token incluyen la identidad de seguridad y la pertenencia a grupos de la cuenta de usuario asociada con el proceso o subproceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

Cada usuario o aplicación que tiene acceso a los recursos de un dominio de Windows debe tener una cuenta en el servidor de Active Directory. Windows usa esta cuenta de usuario para comprobar que el usuario o la aplicación tienen permiso para utilizar un recurso.

Una cuenta de usuario se puede usar para:

-   Permite a los usuarios humanos iniciar sesión en un equipo y obtener acceso a los recursos en función de la identidad de esa cuenta de usuario.
-   Habilitar programas y servicios para que se ejecuten en un contexto de seguridad específico.
-   Administrar el acceso de los usuarios a recursos compartidos, como objetos y sus propiedades, recursos compartidos de red, archivos, directorios, colas de impresión, etc.

Los grupos pueden contener miembros, que son referencias a usuarios y otros grupos. Los grupos también se pueden usar para controlar el acceso a los recursos compartidos. Al asignar permisos para los recursos, por ejemplo, recursos compartidos de archivos, impresoras, etc., los administradores deben asignar esos permisos a un grupo, en lugar de a los usuarios individuales. Los permisos se asignan una vez al grupo, en lugar de varias veces a cada usuario individual. Esto ayuda a simplificar el mantenimiento y la administración de una red.

## <a name="users-compared-to-contacts"></a>Usuarios comparados con contactos

Tanto los usuarios como los contactos se pueden usar para representar usuarios humanos. Sin embargo, un usuario es una entidad de seguridad; un contacto no es.

Un usuario puede usarse para permitir que un usuario humano inicie sesión y acceda a recursos compartidos.

Un contacto solo se usa para la lista de distribución y para el correo electrónico. Sin embargo, un contacto puede contener la mayoría de los datos almacenados en un objeto de usuario, como la dirección, los números de teléfono, etc., ya que tanto el usuario como el contacto se derivan del objeto **ClassSchema** . Un contacto no tiene ningún contexto de seguridad; por lo tanto, no se puede usar un contacto para controlar el acceso a los recursos compartidos y no se puede usar para iniciar sesión en un equipo.

## <a name="users-compared-to-computers"></a>Usuarios comparados con equipos

La clase de objeto de equipo hereda de la clase de objeto de usuario. Un objeto de equipo representa un equipo; sin embargo, el equipo y los servicios locales del equipo suelen requerir acceso a la red y a los recursos compartidos. Cuando el equipo tiene acceso a recursos compartidos, no al usuario que ha iniciado sesión en el equipo, necesita un token de acceso como un usuario humano que ha iniciado sesión como un usuario. Cuando un equipo tiene acceso a la red, usa un token de acceso que contiene el identificador de seguridad de la cuenta de equipo del equipo y los grupos de los que es miembro.

Un servicio se puede ejecutar en el contexto de LocalSystem o de una cuenta de servicio específica. En los equipos que ejecutan Windows 2000, un servicio que se ejecuta en el contexto de la cuenta LocalSystem usa las credenciales del equipo.

 

 




