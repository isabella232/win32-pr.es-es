---
title: RootDSE (ADSI)
description: Cada servidor de directorios tiene una entrada única denominada RootDSE. Proporciona datos sobre el servidor, como sus funcionalidades, la versión LDAP que admite y los contextos de nomenclatura que usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770635"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Cada servidor de directorio tiene una entrada única denominada **RootDSE.** Proporciona datos sobre el servidor, como sus funcionalidades, la versión LDAP que admite y los contextos de nomenclatura que usa.

Por ejemplo, para crear un script o una aplicación que se pueda ejecutar en cualquier entorno Windows dominio. Puede especificar el nombre distintivo, el nombre del servidor o el nombre de dominio al conectarse a Active Directory. Si no tiene esta información, puede usar el **objeto RootDSE** para establecer una conexión. En el ejemplo de código siguiente se cambia la descripción del dominio en cualquier dominio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Al obtener el **atributo defaultNamingContext** de **RootDSE,** puede enlazar al dominio actual, por ejemplo, fabrikam **defaultNamingContext** es DC=Fabrikam, DC=COM.

Para enumerar las propiedades de **RootDSE,** use la [**interfaz IADsPropertyList.**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) no se puede usar para esta tarea.

Para obtener más información, [vea Enlace sin servidor y RootDSE.](/windows/desktop/AD/serverless-binding-and-rootdse)

 

 