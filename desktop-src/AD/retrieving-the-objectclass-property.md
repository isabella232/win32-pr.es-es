---
title: Recuperar el atributo objectClass
description: El atributo objectClass contiene la clase de la que el objeto es una instancia, así como todas las clases de las que se deriva esa clase.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f237efff1e13c7f3498a51f38588c9885fbab76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773099"
---
# <a name="retrieving-the-objectclass-attribute"></a><span data-ttu-id="30fac-103">Recuperar el atributo objectClass</span><span class="sxs-lookup"><span data-stu-id="30fac-103">Retrieving the objectClass Attribute</span></span>

<span data-ttu-id="30fac-104">El atributo **objectClass** contiene la clase de la que el objeto es una instancia, así como todas las clases de las que se deriva esa clase.</span><span class="sxs-lookup"><span data-stu-id="30fac-104">The **objectClass** attribute contains the class of which the object is an instance, as well as all classes from which that class is derived.</span></span> <span data-ttu-id="30fac-105">Por ejemplo, la clase de **usuario** hereda de **Top**, **Person** y **OrganizationalPerson**; por lo tanto, el atributo **objectClass** contiene los nombres de esas clases, así como User.</span><span class="sxs-lookup"><span data-stu-id="30fac-105">For example, the **user** class inherits from **top**, **person**, and **organizationalPerson**; therefore, the **objectClass** attribute contains the names of those classes, as well as user.</span></span> <span data-ttu-id="30fac-106">Por lo tanto, ¿cómo averiguar la clase de la que es instancia el objeto?</span><span class="sxs-lookup"><span data-stu-id="30fac-106">So, how do you find out what class the object is an instance of?</span></span> <span data-ttu-id="30fac-107">El atributo **objectClass** es el único atributo con varios valores que tienen valores ordenados.</span><span class="sxs-lookup"><span data-stu-id="30fac-107">The **objectClass** attribute is the only attribute with multiple values that has ordered values.</span></span> <span data-ttu-id="30fac-108">El primer valor es la parte superior de la jerarquía de clases, que es la clase superior, y el último valor es la clase más derivada, que es la clase de la que el objeto es una instancia de.</span><span class="sxs-lookup"><span data-stu-id="30fac-108">The first value is the top of the class hierarchy, which is the top class, and the last value is the most derived class, which is the class that the object is an instance of.</span></span>

<span data-ttu-id="30fac-109">La siguiente función toma un puntero a una columna que contiene un atributo **objectClass** y devuelve el **objectClass** con instancias del objeto.</span><span class="sxs-lookup"><span data-stu-id="30fac-109">The following function takes a pointer to a column containing an **objectClass** attribute and returns the instantiated **objectClass** of the object.</span></span>


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




