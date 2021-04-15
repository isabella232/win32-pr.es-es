---
title: El método GetEx
description: Algunos atributos pueden almacenar uno o más valores.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, usar GetEx de IADs
- ADSI ADSI, usar, usar el método GetEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656141"
---
# <a name="the-getex-method"></a><span data-ttu-id="e4bc8-105">El método GetEx</span><span class="sxs-lookup"><span data-stu-id="e4bc8-105">The GetEx Method</span></span>

<span data-ttu-id="e4bc8-106">Algunos atributos pueden almacenar uno o más valores.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="e4bc8-107">Por ejemplo, el atributo **otherTelephone** de un objeto de usuario en Active Directory es una propiedad que puede tener cero, uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="e4bc8-108">Los atributos que tienen varios valores se conocen como "atributos multivalor".</span><span class="sxs-lookup"><span data-stu-id="e4bc8-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="e4bc8-109">Si el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) se usa para recuperar un atributo con varios valores, los resultados se deben procesar de forma diferente que si el atributo tiene un valor único.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="e4bc8-110">Los resultados proporcionados por el método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , sin embargo, se procesan de la misma manera, independientemente de si el atributo tiene uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="e4bc8-111">En ambos casos, el método **IADs:: GETEX** devuelve los valores de una matriz.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="e4bc8-112">El método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera propiedades de la memoria caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="e4bc8-113">Si la propiedad especificada no se encuentra en la memoria caché, **IADs:: GETEX** realiza una llamada a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="e4bc8-114">El método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve una matriz de variantes variante sin tener en consideración el número de valores devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="e4bc8-115">Esto es así incluso si el atributo solo contiene un valor.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-115">This is true even if the attribute only contains one value.</span></span>


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="e4bc8-116">También se puede usar el método [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) para los atributos de valor único.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="e4bc8-117">Los resultados de un atributo de un solo valor se procesan de la misma forma que los resultados de un atributo con varios valores.</span><span class="sxs-lookup"><span data-stu-id="e4bc8-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="e4bc8-118">Si no se establece ningún valor para el atributo, [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelve el error "propiedad no encontrada en la memoria caché".</span><span class="sxs-lookup"><span data-stu-id="e4bc8-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




