---
description: Devuelve un valor HRESULT. En este HRESULT, un valor de S \_ OK indica que el método se ejecutó correctamente.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propiedades de control de inscripción de certificados en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541134"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="aaf07-104">Propiedades de control de inscripción de certificados en C++</span><span class="sxs-lookup"><span data-stu-id="aaf07-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="aaf07-105">Al establecer o recuperar una propiedad de control de inscripción de certificados en C++, la llamada al método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aaf07-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="aaf07-106">En este **HRESULT**, un valor de S \_ OK indica que el método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="aaf07-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="aaf07-107">Los programas escritos en C++ pueden recuperar las propiedades de control de inscripción de certificados mediante llamadas a métodos de la forma siguiente.</span><span class="sxs-lookup"><span data-stu-id="aaf07-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="aaf07-108">Donde *PropertyName* especifica el nombre de la propiedad a la que se está accediendo y *pPropValue* es un puntero a una variable del tipo de datos adecuado.</span><span class="sxs-lookup"><span data-stu-id="aaf07-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="aaf07-109">Después de completar correctamente esta llamada al método, *pPropValue* apuntará a la variable que contiene el valor de la propiedad *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="aaf07-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="aaf07-110">Por ejemplo, para recuperar el valor de la propiedad **RootStoreType** , use el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="aaf07-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="aaf07-111">Los programas escritos en C++ pueden establecer las propiedades de control de inscripción de certificados llamando a los métodos de la siguiente forma.</span><span class="sxs-lookup"><span data-stu-id="aaf07-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="aaf07-112">Donde *PropertyName* especifica el nombre de la propiedad a la que se está accediendo y *PropValue* es un valor del tipo de datos adecuado.</span><span class="sxs-lookup"><span data-stu-id="aaf07-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="aaf07-113">Después de completar correctamente esta llamada al método, el nuevo valor de la propiedad *PropertyName* será *PropValue*.</span><span class="sxs-lookup"><span data-stu-id="aaf07-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="aaf07-114">Por ejemplo, para establecer el valor de propiedad para **RootStoreType**, se podría usar el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="aaf07-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



