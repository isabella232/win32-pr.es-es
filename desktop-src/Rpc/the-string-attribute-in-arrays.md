---
title: Atributo de cadena en matrices
description: Puede usar el atributo \ string\ para matrices de caracteres unidimensionales, matrices de caracteres anchos y matrices de bytes que representan cadenas de texto.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361884"
---
# <a name="the-string-attribute-in-arrays"></a>Atributo \[ de cadena en \] matrices

Puede usar el atributo de cadena para matrices de caracteres \[ [](/windows/desktop/Midl/string) unidimensionales, matrices de caracteres anchos y matrices de \] bytes que representan cadenas de texto. Si usa el atributo **\[ \] string,** el código auxiliar de cliente usa las funciones **strlen** o **wstrlen** de la biblioteca de C para contar el número de caracteres de la cadena. Para evitar posibles incoherencias, MIDL **\[ \]** no permite usar el atributo de cadena al mismo tiempo que el primero es , el último es y \[ [ \_](/windows/desktop/Midl/first-is)size \] \[ [ \_](/windows/desktop/Midl/last-is) \] \[ [ \_ son](/windows/desktop/Midl/size-is) \] atributos.

Con las cadenas terminadas en NULL en C, debe permitir el espacio para el carácter nulo al final de la cadena. Por ejemplo, al declarar una cadena que contendrán hasta 80 caracteres, asigne 81 caracteres. El siguiente archivo IDL de ejemplo muestra cómo declarar matrices con el **\[ atributo string. \]**

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 