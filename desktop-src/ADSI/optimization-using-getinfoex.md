---
title: Optimización mediante GetInfoEx
description: Se usa para cargar valores de atributo específicos en la memoria caché local desde el servicio de directorio subyacente.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimización mediante ADSI GetInfoEx
- GetInfoEx ADSI, optimización mediante GetInfoEx de IADs
- ADSI ADSI, usar, optimización mediante el método GetInfoEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359413"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="c63cc-106">Optimización mediante GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="c63cc-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="c63cc-107">El método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se usa para cargar valores de atributo específicos en la memoria caché local desde el servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="c63cc-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="c63cc-108">Este método solo carga los valores de atributo especificados en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="c63cc-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="c63cc-109">El método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) se usa para cargar todos los valores de atributo en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="c63cc-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="c63cc-110">El método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtiene valores actuales específicos para las propiedades de un objeto Active Directory del almacén de directorios subyacente, actualizando los valores almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="c63cc-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="c63cc-111">Sin embargo, si ya existe un valor en la memoria caché de propiedades, al llamar al método [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sin llamar primero a [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para ese atributo se recuperará el valor almacenado en caché en lugar del valor más actual del directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="c63cc-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="c63cc-112">Esto puede hacer que se sobrescriban los valores de atributo actualizados si se ha modificado la memoria caché local, pero los valores no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c63cc-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="c63cc-113">El método sugerido para evitar problemas de almacenamiento en caché consiste en confirmar siempre los cambios del valor de atributo mediante una llamada a **IADs. SetInfo** antes de llamar a [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span><span class="sxs-lookup"><span data-stu-id="c63cc-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="c63cc-114">Recuperar Active Directory atributos construidos</span><span class="sxs-lookup"><span data-stu-id="c63cc-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="c63cc-115">En Active Directory, la mayoría de los atributos construidos se recuperan y se almacenan en la memoria caché cuando se llama al método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) realiza una llamada implícita de **IADs. GetInfo** si la memoria caché está vacía).</span><span class="sxs-lookup"><span data-stu-id="c63cc-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="c63cc-116">Sin embargo, algunos atributos construidos no se recuperan y almacenan en caché automáticamente y, por consiguiente, requieren que se llame explícitamente al método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para recuperarlos.</span><span class="sxs-lookup"><span data-stu-id="c63cc-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="c63cc-117">Por ejemplo, en Active Directory, el atributo [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) no se recupera cuando se llama al método **IADs. GetInfo** y **IADs. Get** devolverá la **propiedad de \_ ADS \_ \_ no \_ encontrada**.</span><span class="sxs-lookup"><span data-stu-id="c63cc-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="c63cc-118">Se debe llamar al método **IADs. GetInfoEx** para recuperar el atributo **canonicalName** .</span><span class="sxs-lookup"><span data-stu-id="c63cc-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="c63cc-119">Estos mismos atributos construidos tampoco se recuperarán mediante la interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) para enumerar los atributos.</span><span class="sxs-lookup"><span data-stu-id="c63cc-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="c63cc-120">Para obtener más información y un ejemplo de código que muestra cómo recuperar todos los valores de atributo, vea el [código de ejemplo para leer un atributo construido](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="c63cc-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 