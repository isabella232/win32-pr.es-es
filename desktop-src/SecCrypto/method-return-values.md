---
description: El valor devuelto para los métodos de interfaz de C++ siempre es de tipo HRESULT; Este valor se puede comprobar para determinar si se ha hecho correctamente o no.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valores devueltos del método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270884"
---
# <a name="method-return-values"></a>Valores devueltos del método

El valor devuelto para los métodos de interfaz de C++ siempre es de tipo **HRESULT**; Este valor se puede comprobar para determinar si se ha hecho correctamente o no. El uso de parámetros de "salida" permite asignar valores a variables durante la llamada de método o propiedad. En el ejemplo siguiente se muestra una llamada al método de C++ para enumerar proveedores.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



En el fragmento de código anterior, se devuelve success o failure a la variable "hr". Si la llamada se ha realizado correctamente, hr se establecerá en S OK y la variable bstrProvider contendrá el nombre \_ del proveedor enumerado.

Una llamada de C++ para recuperar un valor de propiedad sería la siguiente.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Una llamada de C++ para establecer un valor de propiedad sería la siguiente.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



