---
title: Enlazar a Active Directory Domain Services
description: En Active Directory Domain Services, el acto de asociar un objeto de programación a un objeto de Active Directory Domain Services específico se conoce como enlace.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- enlazar a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, enlazar a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998135"
---
# <a name="binding-to-active-directory-domain-services"></a>Enlazar a Active Directory Domain Services

En Active Directory Domain Services, el acto de asociar un objeto de programación a un objeto de Active Directory Domain Services específico se conoce como *enlace*. Cuando un objeto de programación, como un objeto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , está asociado a un objeto de directorio específico, se considera que el objeto de programación está *enlazado al* objeto de directorio.

## <a name="binding-functions-and-methods"></a>Funciones y métodos de enlace

El método para enlazar mediante programación a un objeto Active Directory dependerá de la tecnología de programación que se use. Para obtener más información sobre cómo enlazar a objetos en Active Directory Domain Services con una tecnología de programación específica, vea los temas que se muestran en la tabla siguiente.



| Tecnología de programación                                                                       | Para obtener más información                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Interfaces de servicio de Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Enlazar a un objeto ADSI](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [Protocolo ligero de acceso a directorio](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Establecer una sesión LDAP](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Enlazar a objetos de directorio](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Enlazar cadenas

Todas las funciones y métodos de enlace requieren una cadena de enlace. El formato de la cadena de enlace depende del proveedor. Los Active Directory Domain Services admiten dos proveedores, LDAP y Winnt.

A partir de Windows 2000, el proveedor LDAP se usa para tener acceso a Active Directory Domain Services. La cadena de enlace LDAP puede adoptar una de las siguientes formas:

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

En los ejemplos anteriores, "LDAP:" especifica el proveedor LDAP. "GC:" utiliza el proveedor LDAP para enlazar con el servicio de catálogo global para ejecutar consultas rápidas.

" &lt; nombre &gt; de host" especifica el servidor al que se va a enlazar y es opcional. Si es posible, no especifique un servidor. También es posible enlazar a un objeto en un dominio diferente. Para ello, pase el nombre del sistema de nombres de dominio (DNS) del dominio de destino para " &lt; nombre de host &gt; ". Por ejemplo, para enlazar con el contenedor usuarios en el dominio dominio2 de fabrikam.com, la cadena de enlace sería "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".

" &lt; Object name &gt; " representa un objeto específico en Active Directory Domain Services. El nombre del objeto puede ser un nombre distintivo o un GUID del objeto.

Para obtener más información acerca de las cadenas de enlace LDAP, consulte [ADsPath de LDAP](/windows/desktop/ADSI/ldap-adspath).

En Windows NT 4,0, el proveedor de WinNT se usa para el acceso a datos de directorio como usuarios, grupos de usuarios, equipos, servicios y otros objetos de red en Windows 2000. El proveedor de WinNT en Windows 2000 y sistemas posteriores tiene una funcionalidad limitada en comparación con el proveedor LDAP. Para obtener más información sobre las cadenas de enlace de WinNT, vea [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).

Se puede usar un ADsPath de "LDAP://" o "GC://" para enlazar con la raíz del espacio de nombres. Cuando se enlaza a la raíz del espacio de nombres, el objeto de espacio de nombres proporcionado no contiene ninguna propiedad y contiene el objeto de dominio para LDAP y un objeto contenedor que contiene una réplica parcial de todos los dominios del bosque para GC.

Para obtener más información sobre el enlace en Active Directory Domain Services, vea:

-   [Enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md)
-   [Enlazar con el catálogo global](binding-to-the-global-catalog.md)
-   [Usar objectGUID para enlazar a un objeto](using-objectguid-to-bind-to-an-object.md)
-   [Enlazar a objetos de Well-Known mediante WKGUID](binding-to-well-known-objects-using-wkguid.md)
-   [Enlazar a un objeto mediante un SID](binding-to-an-object-using-a-sid.md)
-   [Habilitar Rename-Safe enlace con la propiedad otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [Autenticación](authentication.md)

 

 
