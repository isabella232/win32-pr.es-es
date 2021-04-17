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
# <a name="certificate-enrollment-control-properties-in-c"></a>Propiedades de control de inscripción de certificados en C++

Al establecer o recuperar una propiedad de control de inscripción de certificados en C++, la llamada al método devuelve un **valor HRESULT**. En este **HRESULT**, un valor de S \_ OK indica que el método se ejecutó correctamente.

Los programas escritos en C++ pueden recuperar las propiedades de control de inscripción de certificados mediante llamadas a métodos de la forma siguiente.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Donde *PropertyName* especifica el nombre de la propiedad a la que se está accediendo y *pPropValue* es un puntero a una variable del tipo de datos adecuado. Después de completar correctamente esta llamada al método, *pPropValue* apuntará a la variable que contiene el valor de la propiedad *PropertyName* .

Por ejemplo, para recuperar el valor de la propiedad **RootStoreType** , use el código siguiente.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



Los programas escritos en C++ pueden establecer las propiedades de control de inscripción de certificados llamando a los métodos de la siguiente forma.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Donde *PropertyName* especifica el nombre de la propiedad a la que se está accediendo y *PropValue* es un valor del tipo de datos adecuado. Después de completar correctamente esta llamada al método, el nuevo valor de la propiedad *PropertyName* será *PropValue*.

Por ejemplo, para establecer el valor de propiedad para **RootStoreType**, se podría usar el código siguiente.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



