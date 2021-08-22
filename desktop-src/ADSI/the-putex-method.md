---
title: Método PutEx
description: El método PutEx de IADs usa el nombre de una propiedad para guardar una propiedad con uno o varios valores en la caché de propiedades.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI , about
- ADSI ADSI , código de ejemplo Visual Basic , mediante el método PutEx
- ADSI de propiedades, guardar una propiedad única o multivalor en la caché de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c07fad5d22110d345b71a763add5483d7f0be5f6ae2c36557eb7f1563561c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023173"
---
# <a name="the-putex-method"></a>Método PutEx

El [**método IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa el nombre de una propiedad para guardar una propiedad con uno o varios valores en la caché de propiedades. Esto sobrescribe cualquier valor actualmente en la caché de propiedades. Los valores de la memoria caché no se escriben en el servicio de directorio subyacente hasta que se produce un [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) El primer argumento de **PutEx** indica si desea reemplazar o agregar a los valores existentes para la propiedad . En el ejemplo siguiente, los valores existentes del atributo **description** se borran en la memoria caché cuando se llama a **PutEx** y se borran en el servidor cuando se llama **a SetInfo.**


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



 

 




