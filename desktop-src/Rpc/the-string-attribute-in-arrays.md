---
title: Atributo de cadena en matrices
description: Puede usar el atributo \ String \ para matrices de caracteres unidimensionales, matrices de caracteres anchos y matrices de bytes que representan cadenas de texto.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149455"
---
# <a name="the-string-attribute-in-arrays"></a>\[ \] Atributo de cadena en matrices

Puede usar el atributo \[ [String](/windows/desktop/Midl/string) \] para matrices de caracteres unidimensionales, matrices de caracteres anchos y matrices de bytes que representan cadenas de texto. Si usa el atributo **\[ String \]** , el código auxiliar de cliente usa las funciones de la biblioteca C **strlen** o **wstrlen** para contar el número de caracteres de la cadena. Para evitar posibles incoherencias, MIDL no permite usar el atributo de **\[ \] cadena** al mismo tiempo que el \[ [primero \_ es](/windows/desktop/Midl/first-is), el \] \[ [último \_ es](/windows/desktop/Midl/last-is)y el \] \[ [tamaño \_ es](/windows/desktop/Midl/size-is) \] atributos.

Con cadenas terminadas en null en C, debe permitir el espacio para el carácter nulo al final de la cadena. Por ejemplo, al declarar una cadena que contenga hasta 80 caracteres, asigne 81 caracteres. En el siguiente archivo IDL de ejemplo se muestra cómo declarar matrices con el atributo de **\[ cadena \]** .

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

 

 