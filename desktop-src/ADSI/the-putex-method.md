---
title: El método PutEx
description: El método PutEx de IADs utiliza el nombre de una propiedad para guardar una propiedad con uno o varios valores en la memoria caché de propiedades.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI, acerca de
- ADSI ADSI, Visual Basic de código de ejemplo, utilizar el método PutEx
- propiedades ADSI, guardar una propiedad única o con varios valores en la caché de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903022"
---
# <a name="the-putex-method"></a>El método PutEx

El método [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa el nombre de una propiedad para guardar una propiedad con uno o varios valores en la memoria caché de propiedades. Esto sobrescribe cualquier valor que se encuentre actualmente en la caché de propiedades. Los valores de la memoria caché no se escriben en el servicio de directorio subyacente hasta que se produce un [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . El primer argumento de **PutEx** indica si desea reemplazar o agregar a cualquier valor existente para la propiedad. En el ejemplo siguiente, los valores existentes del atributo **Description** se borran en la memoria caché cuando se llama a **PutEx** y se borran en el servidor cuando se llama a **SetInfo** .


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




