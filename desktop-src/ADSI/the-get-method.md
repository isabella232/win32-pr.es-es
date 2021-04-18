---
title: El método get
description: El método get de IADs se utiliza para recuperar los atributos con nombre individuales de un objeto de directorio.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Obtener ADSI mediante IADs Get
- ADSI ADSI, usar, usar el método get de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656142"
---
# <a name="the-get-method"></a><span data-ttu-id="b3f37-105">El método get</span><span class="sxs-lookup"><span data-stu-id="b3f37-105">The Get Method</span></span>

<span data-ttu-id="b3f37-106">El método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) se utiliza para recuperar los atributos con nombre individuales de un objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="b3f37-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="b3f37-107">En el ejemplo de código siguiente se usa el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar un atributo con nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="b3f37-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



<span data-ttu-id="b3f37-108">En los lenguajes de automatización, también se puede tener acceso a los atributos con nombre directamente mediante la notación de puntos.</span><span class="sxs-lookup"><span data-stu-id="b3f37-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="b3f37-109">Por ejemplo, **objeto. Get ("distinguishedName")** es idéntico a **Object. distinguishedName**.</span><span class="sxs-lookup"><span data-stu-id="b3f37-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="b3f37-110">El siguiente ejemplo de código es idéntico al ejemplo anterior, salvo que se tiene acceso al atributo **distinguishedName** mediante la notación de puntos.</span><span class="sxs-lookup"><span data-stu-id="b3f37-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



<span data-ttu-id="b3f37-111">Si no se establece un valor en el objeto, el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) devolverá el error "propiedad no encontrada en la memoria caché".</span><span class="sxs-lookup"><span data-stu-id="b3f37-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




