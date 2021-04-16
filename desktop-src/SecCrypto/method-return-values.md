---
description: El valor devuelto para los métodos de interfaz de C++ es siempre de tipo HRESULT; Este valor se puede comprobar para determinar si se ha realizado correctamente o no.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valores devueltos del método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666531"
---
# <a name="method-return-values"></a><span data-ttu-id="88fc7-103">Valores devueltos del método</span><span class="sxs-lookup"><span data-stu-id="88fc7-103">Method Return Values</span></span>

<span data-ttu-id="88fc7-104">El valor devuelto para los métodos de interfaz de C++ es siempre de tipo **HRESULT**; Este valor se puede comprobar para determinar si se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="88fc7-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="88fc7-105">El uso de los parámetros "Output" permite asignar valores a las variables durante la llamada de método o propiedad.</span><span class="sxs-lookup"><span data-stu-id="88fc7-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="88fc7-106">En el ejemplo siguiente se muestra una llamada al método de C++ para enumerar los proveedores.</span><span class="sxs-lookup"><span data-stu-id="88fc7-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="88fc7-107">En el fragmento de código anterior, se devuelve SUCCESS o Failure a la variable "HR".</span><span class="sxs-lookup"><span data-stu-id="88fc7-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="88fc7-108">Si la llamada se realizó correctamente, HR se establecerá en S \_ OK y la variable bstrProvider contendrá el nombre del proveedor enumerado.</span><span class="sxs-lookup"><span data-stu-id="88fc7-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="88fc7-109">Una llamada de C++ para recuperar un valor de propiedad sería como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="88fc7-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="88fc7-110">Una llamada de C++ para establecer un valor de propiedad sería como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="88fc7-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



