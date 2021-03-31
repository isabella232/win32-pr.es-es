---
title: El atributo size_is
description: El atributo \ size \_ es \ se asocia a una constante, expresión o variable de tipo entero que especifica el tamaño de asignación de la matriz.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904658"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="5aec5-104">El \[ tamaño \_ es \] Attribute</span><span class="sxs-lookup"><span data-stu-id="5aec5-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="5aec5-105">El \[ [atributo \_ size](/windows/desktop/Midl/size-is) está \] asociado a una constante, expresión o variable de tipo entero que especifica el tamaño de asignación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5aec5-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="5aec5-106">Considere una matriz de caracteres cuya longitud esté determinada por la entrada del usuario:</span><span class="sxs-lookup"><span data-stu-id="5aec5-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="5aec5-107">El asterisco ( \* ) que marca el marcador de posición para la dimensión de la matriz de variables es opcional.</span><span class="sxs-lookup"><span data-stu-id="5aec5-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="5aec5-108">El código auxiliar del servidor debe asignar memoria en el servidor que corresponda a la memoria en el cliente para ese parámetro.</span><span class="sxs-lookup"><span data-stu-id="5aec5-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="5aec5-109">La variable que especifica el tamaño siempre debe ser al menos un \[ parámetro [in](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="5aec5-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="5aec5-110">El atributo direccional **\[ in \]** es necesario para que el valor de tamaño se defina en la entrada al código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="5aec5-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="5aec5-111">Este valor de tamaño proporciona información que el código auxiliar del servidor requiere para asignar la memoria.</span><span class="sxs-lookup"><span data-stu-id="5aec5-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="5aec5-112">El parámetro de tamaño también puede ser \[ in, [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="5aec5-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="5aec5-113">Esto es útil si, por ejemplo, la matriz que envía el cliente no es lo suficientemente grande para los datos que el servidor necesita almacenar en él.</span><span class="sxs-lookup"><span data-stu-id="5aec5-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="5aec5-114">Puede usar un parámetro **\[ in, out \]** size para devolver el tamaño requerido al programa cliente.</span><span class="sxs-lookup"><span data-stu-id="5aec5-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aec5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5aec5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aec5-116">Varios niveles de punteros</span><span class="sxs-lookup"><span data-stu-id="5aec5-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 