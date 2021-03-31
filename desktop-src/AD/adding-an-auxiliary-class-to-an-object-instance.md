---
title: Agregar una clase auxiliar a una instancia de objeto
description: En los siguientes ejemplos de código se muestra cómo usar ADSI y LDAP para agregar dinámicamente una clase auxiliar a una instancia de objeto existente.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077572"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="65862-103">Agregar una clase auxiliar a una instancia de objeto</span><span class="sxs-lookup"><span data-stu-id="65862-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="65862-104">En los siguientes ejemplos de código se muestra cómo usar ADSI y LDAP para agregar dinámicamente una clase auxiliar a una instancia de objeto existente.</span><span class="sxs-lookup"><span data-stu-id="65862-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="65862-105">En los ejemplos se supone que una clase auxiliar denominada **Vehicle** se define en el esquema de Active Directory y que la clase **Vehicle** tiene un atributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="65862-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="65862-106">Cuando agrega dinámicamente una clase auxiliar a una instancia de objeto, debe especificar simultáneamente los valores de los atributos **mustHave** obligatorios en la clase.</span><span class="sxs-lookup"><span data-stu-id="65862-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="65862-107">En los siguientes ejemplos se muestra cómo hacerlo con el atributo "Vin", que se supone que es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65862-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="65862-108">En el siguiente ejemplo de C++ se enlaza a un objeto y se usa [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) para anexar la clase auxiliar a la lista de clases en la propiedad **objectClass** del objeto.</span><span class="sxs-lookup"><span data-stu-id="65862-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="65862-109">A continuación, en el ejemplo se usa [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer el valor del atributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="65862-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="65862-110">Por último, llama a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.</span><span class="sxs-lookup"><span data-stu-id="65862-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 