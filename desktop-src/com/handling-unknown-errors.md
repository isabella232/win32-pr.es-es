---
title: Control de errores desconocidos
description: Control de errores desconocidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076285"
---
# <a name="handling-unknown-errors"></a>Control de errores desconocidos

Es válido devolver un código de estado solo desde la implementación de un método de interfaz autorizada como devuelto legalmente. Si no se observa esta regla, se invita a la posibilidad de que se produzca un conflicto entre los valores devueltos del código de error y los autorizados por la aplicación. Preste especial atención a este posible problema al propagar los códigos de error de las funciones a las que se llama internamente.

Las aplicaciones que llaman a interfaces deben tratar cualquier código de error devuelto desconocido (en lugar de un código correcto) como sinónimo de E \_ inesperado. La práctica de controlar códigos de error desconocidos es necesaria para los clientes de las interfaces y funciones definidas por COM. Dado que la práctica típica de programación consiste en controlar algunos códigos de error específicos en detalle y tratar el resto de forma genérica, se cumple fácilmente este requisito de administrar los códigos de error inesperados o desconocidos.

Es importante controlar todos los posibles errores al llamar a un método de interfaz. Si no lo hace, la aplicación se bloqueará, se dañarán los datos o se hará vulnerable a las vulnerabilidades de seguridad. En el ejemplo de código siguiente se muestra la forma recomendada de controlar los errores desconocidos:


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



La siguiente comprobación de errores suele usarse con esas rutinas que no devuelven nada especial (que no sea \_ correcto o algún error inesperado):


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

 

 




