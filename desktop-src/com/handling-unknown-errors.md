---
title: Control de errores desconocidos
description: Control de errores desconocidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973642"
---
# <a name="handling-unknown-errors"></a>Control de errores desconocidos

Es legal devolver un código de estado solo desde la implementación de un método de interfaz autorizado como legalmente recuperable. Si no se observa esta regla, se invita a la posibilidad de conflicto entre los valores de código de error devueltos y los autorizados por la aplicación. Preste especial atención a este posible problema al propagar códigos de error de funciones a las que se llama internamente.

Las aplicaciones que llaman a interfaces deben tratar cualquier código de error devuelto desconocido (en lugar de un código correcto) como sinónimo de E \_ UNEXPECTED. Esta práctica de control de códigos de error desconocidos es necesaria para los clientes de las interfaces y funciones definidas por COM. Dado que la práctica de programación típica es controlar algunos códigos de error específicos en detalle y tratar el resto genéricamente, este requisito de controlar códigos de error inesperados o desconocidos se cumple fácilmente.

Es importante controlar todos los errores posibles al llamar a un método de interfaz. Si no lo hace, la aplicación podría bloquearse, dañar los datos o ser vulnerable a vulnerabilidades de seguridad. En el ejemplo de código siguiente se muestra la manera recomendada de controlar errores desconocidos:


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



La siguiente comprobación de errores se usa a menudo con las rutinas que no devuelven nada especial (aparte de S \_ OK o algún error inesperado):


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

 




