---
title: Optimize (atributo)
description: El atributo \ Optimize \ ACF se usa para ajustar el nivel de degradado para calcular las referencias de los datos.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- optimizar el atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651326"
---
# <a name="optimize-attribute"></a><span data-ttu-id="74e01-104">Optimize (atributo)</span><span class="sxs-lookup"><span data-stu-id="74e01-104">optimize attribute</span></span>

<span data-ttu-id="74e01-105">El atributo **\[ apoptimize \]** ACF se usa para ajustar el nivel de degradado para calcular las referencias de los datos.</span><span class="sxs-lookup"><span data-stu-id="74e01-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="74e01-106">Esta palabra clave es superceeded y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="74e01-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="74e01-107">En su lugar, las compilaciones de MIDL actuales deben usar [**/Oicf**](-oi.md)[**/Robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="74e01-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="74e01-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e01-109">*optimización: opciones*</span><span class="sxs-lookup"><span data-stu-id="74e01-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="74e01-110">Especifica el método de cálculo de referencias de datos.</span><span class="sxs-lookup"><span data-stu-id="74e01-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="74e01-111">Use "s" para la serialización en modo mixto o "i" para el cálculo de referencias interpretado.</span><span class="sxs-lookup"><span data-stu-id="74e01-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74e01-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74e01-112">Remarks</span></span>

<span data-ttu-id="74e01-113">Esta versión de RPC proporciona dos métodos para calcular las referencias de datos: modo mixto ("s") e interpretado ("i").</span><span class="sxs-lookup"><span data-stu-id="74e01-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="74e01-114">Estos métodos corresponden a los modificadores de la línea de comandos [**/os**](-os.md) y [**/OI**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="74e01-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="74e01-115">El método interpretado calcula las referencias de los datos completamente sin conexión.</span><span class="sxs-lookup"><span data-stu-id="74e01-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="74e01-116">Aunque esto puede reducir considerablemente el tamaño del código auxiliar, el rendimiento puede verse afectado.</span><span class="sxs-lookup"><span data-stu-id="74e01-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="74e01-117">Si el rendimiento es un problema, el método de modo mixto puede ser el mejor enfoque.</span><span class="sxs-lookup"><span data-stu-id="74e01-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="74e01-118">El modo mixto permite que el compilador de MIDL realice la determinación entre los datos que se van a serializar insertados y los que se calcularán mediante una llamada a una biblioteca de vínculos dinámicos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="74e01-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="74e01-119">Si muchos procedimientos utilizan los mismos tipos de datos, se puede llamar a un único procedimiento repetidamente para calcular las referencias de los datos.</span><span class="sxs-lookup"><span data-stu-id="74e01-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="74e01-120">De esta manera, los datos que son más adecuados para el cálculo de referencias en línea se procesan en línea mientras que otros datos se pueden serializar de forma más eficaz sin conexión.</span><span class="sxs-lookup"><span data-stu-id="74e01-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="74e01-121">Tenga en cuenta que el atributo **\[ Optimize \]** se puede usar como atributo de interfaz o como atributo de operación.</span><span class="sxs-lookup"><span data-stu-id="74e01-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="74e01-122">Si se usa como atributo de interfaz, establece el valor predeterminado para toda la interfaz, invalidando los modificadores de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="74e01-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="74e01-123">Sin embargo, si se usa como atributo de operación, solo afecta a esa operación, invalidando los modificadores de la línea de comandos y el valor predeterminado de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="74e01-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="74e01-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="74e01-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="74e01-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="74e01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e01-126">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="74e01-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="74e01-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="74e01-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="74e01-128">**/Os**</span><span class="sxs-lookup"><span data-stu-id="74e01-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="74e01-129">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="74e01-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




