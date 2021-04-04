---
title: Servicios de dominio de Active Directory
description: Microsoft Active Directory Domain Services es la base de las redes distribuidas basadas en los sistemas operativos Windows 2000 Server, Windows Server 2003 y Microsoft Windows Server 2008 que usan controladores de dominio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory de Active Directory, página de inicio
- Active Directory de Active Directory Domain Services, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078572"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>Propósito

Microsoft Active Directory Domain Services es la base de las redes distribuidas basadas en los sistemas operativos Windows 2000 Server, Windows Server 2003 y Microsoft Windows Server 2008 que usan controladores de dominio. Active Directory Domain Services proporcionan almacenamiento jerárquico de datos seguro y estructurado para objetos en una red como usuarios, equipos, impresoras y servicios. Active Directory Domain Services proporcionan compatibilidad para buscar y trabajar con estos objetos.

En esta guía se proporciona información general sobre Active Directory Domain Services y el código de ejemplo para tareas básicas, como buscar objetos y leer propiedades, para tareas más avanzadas, como la publicación de servicio.

Windows 2000 Server y los sistemas operativos posteriores proporcionan una interfaz de usuario para que los usuarios y administradores puedan trabajar con los objetos y datos de Active Directory Domain Services. En esta guía se describe cómo extender y personalizar esa interfaz de usuario. También se describe cómo extender Active Directory Domain Services definiendo nuevas clases de objetos y atributos.

> [!Note]  
> La siguiente documentación es para programadores de equipos. Si es un usuario final que está intentando depurar un error de impresión o un problema de la red doméstica, consulte los foros de la [comunidad de Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Donde sea aplicable

Los administradores de red escriben scripts y aplicaciones que tienen acceso a Active Directory Domain Services para automatizar las tareas administrativas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos para los recursos de red.

Los fabricantes de software independientes y los desarrolladores de usuarios finales pueden usar Active Directory Domain Services programación para habilitar los productos y las aplicaciones en el directorio. Los servicios pueden publicarse en Active Directory Domain Services; los clientes pueden usar Active Directory Domain Services para buscar servicios y ambos pueden usar Active Directory Domain Services para buscar otros objetos en una red y trabajar con ellos.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Las aplicaciones que tienen acceso a los datos de Active Directory Domain Services pueden escribirse mediante la API de [interfaces de servicio Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , la API de [Protocolo ligero de acceso a directorios](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) o el espacio de nombres [System. DirectoryServices](/dotnet/api/system.directoryservices) .

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Active Directory Domain Services ejecutar en controladores de dominio de Windows 2000 y versiones posteriores. Sin embargo, las aplicaciones cliente se pueden escribir y ejecutar en Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 y Windows 95.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Información general sobre Active Directory Domain Services.

</dd> <dt>

[Uso de Active Directory Domain Services](using-active-directory-domain-services.md)
</dt> <dd>

Active Directory Domain Services guía de programación.

</dd> <dt>

[Referencia de Active Directory Domain Services](active-directory-domain-services-reference.md)
</dt> <dd>

Referencia de programación de Active Directory Domain Services.

</dd> </dl>

 

 