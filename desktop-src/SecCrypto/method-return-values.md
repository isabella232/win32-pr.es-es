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
# <a name="method-return-values"></a>Valores devueltos del método

El valor devuelto para los métodos de interfaz de C++ es siempre de tipo **HRESULT**; Este valor se puede comprobar para determinar si se ha realizado correctamente o no. El uso de los parámetros "Output" permite asignar valores a las variables durante la llamada de método o propiedad. En el ejemplo siguiente se muestra una llamada al método de C++ para enumerar los proveedores.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



En el fragmento de código anterior, se devuelve SUCCESS o Failure a la variable "HR". Si la llamada se realizó correctamente, HR se establecerá en S \_ OK y la variable bstrProvider contendrá el nombre del proveedor enumerado.

Una llamada de C++ para recuperar un valor de propiedad sería como se indica a continuación.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Una llamada de C++ para establecer un valor de propiedad sería como se indica a continuación.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



