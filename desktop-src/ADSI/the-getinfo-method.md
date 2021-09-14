---
title: El método GetInfo
description: El método GetInfo de IADs carga todos los valores de atributo de un objeto ADSI en la memoria caché local desde el servicio de directorio subyacente.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI , mediante IADs GetInfo
- ADSI ADSI , using,using the IADs GetInfo method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172181"
---
# <a name="the-getinfo-method"></a>El método GetInfo

El [**método IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carga todos los valores de atributo de un objeto ADSI en la memoria caché local desde el servicio de directorio subyacente. El [**método IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se usa para cargar valores de atributo específicos en la memoria caché local. Para obtener más información sobre el uso **del método IADs::GetInfoEx,** vea [Optimización mediante GetInfoEx](optimization-using-getinfoex.md).

ADSI realizará una llamada [**implícita a IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) cuando se llame al método [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) para un atributo específico y no se encuentra ningún valor en la caché local. Cuando **se ha llamado a IADs::GetInfo,** no se repite una llamada implícita. Sin embargo, si ya existe un valor en la caché de propiedades, al llamar al método **IADs::Get** o **IADs::GetEx** sin llamar primero a **IADs::GetInfo,** se recuperará el valor almacenado en caché en lugar del valor más actual del directorio subyacente. Esto puede hacer que los valores de atributo actualizados se sobrescriban si se ha modificado la memoria caché local, pero los valores no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Para evitar problemas de almacenamiento en caché, confirme los cambios de valor de atributo llamando a **IADs::SetInfo** antes de llamar a **IADs::GetInfo**.


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



Algunos servicios de directorio no devuelven todos los valores de atributo de un objeto en respuesta a una llamada [**a IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) En estos casos, use [**el método IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para cargar estos valores en la memoria caché local.

 

 




