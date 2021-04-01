---
title: RootDSE (ADSI)
description: Cada servidor de directorio tiene una entrada única denominada RootDSE. Proporciona datos sobre el servidor, como sus capacidades, la versión de LDAP que admite y los contextos de nomenclatura que usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793833"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Cada servidor de directorio tiene una entrada única denominada **RootDSE**. Proporciona datos sobre el servidor, como sus capacidades, la versión de LDAP que admite y los contextos de nomenclatura que usa.

Por ejemplo, para crear un script, o una aplicación, que se pueda ejecutar en cualquier entorno de dominio de Windows. Puede especificar el nombre distintivo, el nombre del servidor o el nombre de dominio al conectarse a Active Directory. Si no dispone de esta información, puede usar el objeto **RootDSE** para establecer una conexión. En el siguiente ejemplo de código se cambia la descripción del dominio en cualquier dominio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Al obtener el atributo **defaultNamingContext** de **RootDSE**, puede enlazar con el dominio actual; por ejemplo, Fabrikam **defaultNamingContext** es DC = Fabrikam, DC = com.

Para enumerar las propiedades de **RootDSE**, use la interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . No se puede usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para esta tarea.

Para obtener más información, vea [enlace sin servidor y RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 