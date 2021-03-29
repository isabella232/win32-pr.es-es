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
# <a name="the-putex-method"></a><span data-ttu-id="41ea5-106">El método PutEx</span><span class="sxs-lookup"><span data-stu-id="41ea5-106">The PutEx Method</span></span>

<span data-ttu-id="41ea5-107">El método [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa el nombre de una propiedad para guardar una propiedad con uno o varios valores en la memoria caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="41ea5-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="41ea5-108">Esto sobrescribe cualquier valor que se encuentre actualmente en la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="41ea5-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="41ea5-109">Los valores de la memoria caché no se escriben en el servicio de directorio subyacente hasta que se produce un [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="41ea5-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="41ea5-110">El primer argumento de **PutEx** indica si desea reemplazar o agregar a cualquier valor existente para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="41ea5-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="41ea5-111">En el ejemplo siguiente, los valores existentes del atributo **Description** se borran en la memoria caché cuando se llama a **PutEx** y se borran en el servidor cuando se llama a **SetInfo** .</span><span class="sxs-lookup"><span data-stu-id="41ea5-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


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



 

 




