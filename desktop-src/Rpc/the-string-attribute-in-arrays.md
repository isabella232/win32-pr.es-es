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
# <a name="the-string-attribute-in-arrays"></a><span data-ttu-id="f5101-104">\[ \] Atributo de cadena en matrices</span><span class="sxs-lookup"><span data-stu-id="f5101-104">The \[string\] Attribute in Arrays</span></span>

<span data-ttu-id="f5101-105">Puede usar el atributo \[ [String](/windows/desktop/Midl/string) \] para matrices de caracteres unidimensionales, matrices de caracteres anchos y matrices de bytes que representan cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="f5101-105">You can use the \[ [string](/windows/desktop/Midl/string)\] attribute for one-dimensional character arrays, wide-character arrays, and byte arrays that represent text strings.</span></span> <span data-ttu-id="f5101-106">Si usa el atributo **\[ String \]** , el código auxiliar de cliente usa las funciones de la biblioteca C **strlen** o **wstrlen** para contar el número de caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f5101-106">If you use the **\[string\]** attribute, the client stub uses the C-library functions **strlen** or **wstrlen** to count the number of characters in the string.</span></span> <span data-ttu-id="f5101-107">Para evitar posibles incoherencias, MIDL no permite usar el atributo de **\[ \] cadena** al mismo tiempo que el \[ [primero \_ es](/windows/desktop/Midl/first-is), el \] \[ [último \_ es](/windows/desktop/Midl/last-is)y el \] \[ [tamaño \_ es](/windows/desktop/Midl/size-is) \] atributos.</span><span class="sxs-lookup"><span data-stu-id="f5101-107">To avoid possible inconsistencies, MIDL does not let you use the **\[string\]** attribute at the same time as the \[ [first\_is](/windows/desktop/Midl/first-is)\], \[ [last\_is](/windows/desktop/Midl/last-is)\], and \[ [size\_is](/windows/desktop/Midl/size-is)\] attributes.</span></span>

<span data-ttu-id="f5101-108">Con cadenas terminadas en null en C, debe permitir el espacio para el carácter nulo al final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f5101-108">With null-terminated strings in C, you must allow space for the null character at the end of the string.</span></span> <span data-ttu-id="f5101-109">Por ejemplo, al declarar una cadena que contenga hasta 80 caracteres, asigne 81 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5101-109">For example, when declaring a string that will hold up to 80 characters, allocate 81 characters.</span></span> <span data-ttu-id="f5101-110">En el siguiente archivo IDL de ejemplo se muestra cómo declarar matrices con el atributo de **\[ cadena \]** .</span><span class="sxs-lookup"><span data-stu-id="f5101-110">The following sample IDL file demonstrates how to declare arrays with the **\[string\]** attribute.</span></span>

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

 

 