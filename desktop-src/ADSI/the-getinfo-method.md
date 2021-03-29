---
title: El método GetInfo
description: El método GetInfo de IADs carga todos los valores de atributo de un objeto ADSI en la memoria caché local desde el servicio de directorio subyacente.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- ADSI de GetInfo, uso de GetInfo de IADs
- ADSI ADSI, usar, usar el método GetInfo de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772907"
---
# <a name="the-getinfo-method"></a><span data-ttu-id="328ba-105">El método GetInfo</span><span class="sxs-lookup"><span data-stu-id="328ba-105">The GetInfo Method</span></span>

<span data-ttu-id="328ba-106">El método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carga todos los valores de atributo de un objeto ADSI en la memoria caché local desde el servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="328ba-106">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method loads all of the attribute values for an ADSI object into the local cache from the underlying directory service.</span></span> <span data-ttu-id="328ba-107">El método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se usa para cargar valores de atributo específicos en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="328ba-107">The [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache.</span></span> <span data-ttu-id="328ba-108">Para obtener más información sobre el uso del método **IADs:: GetInfoEx** , vea [optimización con GetInfoEx](optimization-using-getinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="328ba-108">For more information about using the **IADs::GetInfoEx** method, see [Optimization Using GetInfoEx](optimization-using-getinfoex.md).</span></span>

<span data-ttu-id="328ba-109">ADSI realizará una llamada a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita cuando se llama al método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) para un atributo concreto y no se encuentra ningún valor en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="328ba-109">ADSI will make an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call when the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method is called for a specific attribute and no value is found in the local cache.</span></span> <span data-ttu-id="328ba-110">Cuando se llama a **IADs:: GetInfo** , no se repite una llamada implícita.</span><span class="sxs-lookup"><span data-stu-id="328ba-110">When **IADs::GetInfo** has been called, an implicit call is not repeated.</span></span> <span data-ttu-id="328ba-111">Sin embargo, si ya existe un valor en la memoria caché de propiedades, al llamar al método **IADs:: get** o **IADs:: GETEX** sin llamar primero a **IADs:: GetInfo** se recuperará el valor almacenado en caché en lugar del valor más actual del directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="328ba-111">If a value already exists in the property cache, however, calling the **IADs::Get** or **IADs::GetEx** method without first calling **IADs::GetInfo** will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="328ba-112">Esto puede hacer que se sobrescriban los valores de atributo actualizados si se ha modificado la memoria caché local, pero los valores no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="328ba-112">This can cause updated attribute values to be overwritten if the local cache has been modified but the values have not been committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="328ba-113">Para evitar problemas de almacenamiento en caché, confirme los cambios del valor de atributo mediante una llamada a **IADs:: SetInfo** antes de llamar a **IADs:: GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="328ba-113">To avoid caching problems, commit attribute value changes by calling **IADs::SetInfo** before calling **IADs::GetInfo**.</span></span>


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



<span data-ttu-id="328ba-114">Algunos servicios de directorio no devuelven todos los valores de atributo de un objeto en respuesta a una llamada a [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="328ba-114">Some directory services do not return all attribute values for an object in response to a [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span> <span data-ttu-id="328ba-115">En estos casos, use el método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para cargar estos valores en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="328ba-115">In these cases, use the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method to load these values into the local cache.</span></span>

 

 




