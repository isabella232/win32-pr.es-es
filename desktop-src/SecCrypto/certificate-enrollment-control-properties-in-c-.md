---
description: Devuelve un valor HRESULT. En este HRESULT, un valor de S \_ OK indica que el método se ejecutó correctamente.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propiedades del control de inscripción de certificados en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771924"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Propiedades del control de inscripción de certificados en C++

Al establecer o recuperar una propiedad control de inscripción de certificados en C++, la llamada al método devuelve **un valor HRESULT**. En este **HRESULT**, un valor de S \_ OK indica que el método se ejecutó correctamente.

Los programas escritos en C++ pueden recuperar las propiedades del control de inscripción de certificados mediante llamadas de método con el formato siguiente.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Donde *propertyName* especifica el nombre de la propiedad a la que se tiene acceso y *pPropValue* es un puntero a una variable del tipo de datos adecuado. Después de completar correctamente esta llamada de método, *pPropValue* apuntará a la variable que contiene el valor de la *propiedad propertyName.*

Por ejemplo, para recuperar el valor de la **propiedad RootStoreType,** use el código siguiente.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



Los programas escritos en C++ pueden establecer las propiedades del control de inscripción de certificados llamando a métodos con el formato siguiente.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Donde *propertyName* especifica el nombre de la propiedad a la que se tiene acceso y *PropValue* es un valor del tipo de datos adecuado. Después de completar correctamente esta llamada al método , el nuevo valor de la *propiedad propertyName* será *PropValue.*

Por ejemplo, para establecer el valor de propiedad para **RootStoreType**, se podría usar el código siguiente.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



