---
title: Usuarios en Active Directory Domain Services
description: Active Directory Domain Services incluye un servicio de directorio que almacena el dominio, el usuario, el grupo de usuarios y los datos de seguridad.
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Usuarios en Active Directory Domain Services Active Directory
- usuarios, servicios de dominio de Active Directory
- Active Directory Domain Services, usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077487"
---
# <a name="users-in-active-directory-domain-services"></a>Usuarios en Active Directory Domain Services

Active Directory Domain Services incluye un servicio de directorio que almacena el dominio, el usuario, el grupo de usuarios y los datos de seguridad.

En Windows NT 4,0 y versiones anteriores, puede usar funciones como [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel), etc., para administrar usuarios, grupos de usuarios y otros elementos de red. En Windows 2000 y versiones posteriores de Windows, ADSI proporciona un acceso uniforme y seguro a estos elementos y sus propiedades. Tenga en cuenta que ADSI proporciona un proveedor de Windows NT 4,0 que le permite usar ADSI para administrar usuarios, grupos de usuarios y equipos en sistemas Windows NT 4,0. También hay proveedores para Windows Server 2008 Enterprise (instalación Server Core), Microsoft Exchange 5,5, Microsoft Internet Information Server (IIS), Novell Servicios de directorio NetWare (NDS) y Novell NetWare 3. Es decir, un único conjunto de métodos normalizados para administrar usuarios y grupos de usuarios para Windows NT, NDS y NetWare 3.

Además, Windows 2000 es un directorio de varios maestros. Es decir, se pueden realizar cambios en los usuarios, grupos de usuarios y otros datos almacenados en el directorio en cualquier controlador de dominio. En Windows 2000, no es necesario encontrar el controlador de dominio principal (PDC) y realizar cambios en el usuario y el grupo de usuarios en el PDC.

Windows 2000 también incorpora un nuevo espacio de nombres jerárquico dentro de un dominio denominado unidad organizativa (OU). Una unidad organizativa puede contener equipos, usuarios, grupos de usuarios y otros objetos de red. Normalmente, una unidad organizativa se usa con el fin de agrupar elementos con fines administrativos, como la delegación de derechos administrativos y la asignación de directivas al grupo como una sola unidad.

Los dominios, las unidades organizativas, los usuarios, los grupos de usuarios, los equipos y otros elementos de red se almacenan como objetos en Active Directory Domain Services. En Windows 2000 y versiones posteriores de Windows, sigue agregando usuarios, grupos de usuarios y equipos a un dominio. Sin embargo, ahora tiene la opción de agregar estos objetos a un contenedor de unidades organizativas o cualquier otro tipo de contenedor que el objeto que desea agregar defina en el atributo **possSuperiors** del objeto **ClassSchema** ; se trata de un atributo del objeto **ClassSchema** de un objeto y este atributo restringe los tipos de objetos que pueden contener ese objeto.

 

 