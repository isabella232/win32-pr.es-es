---
description: El valor devuelto para los métodos de interfaz de C++ siempre es de tipo HRESULT; Este valor se puede comprobar para determinar si se ha hecho correctamente o no.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valores devueltos del método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073df1d306fb991d7e1347ff90a21d578bf42583c642a694de3160b405963a28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100765"
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



 

 



