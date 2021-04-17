---
title: Parámetro/os
description: El modificador/os especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /Os (modificador) MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676289"
---
# <a name="os-switch"></a><span data-ttu-id="57aa4-104">Parámetro/os</span><span class="sxs-lookup"><span data-stu-id="57aa4-104">/Os switch</span></span>

<span data-ttu-id="57aa4-105">El modificador **/os** especifica el método de modo mixto para serializar el código auxiliar pasado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57aa4-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="57aa4-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="57aa4-106">Switch Options</span></span>

<span data-ttu-id="57aa4-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="57aa4-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="57aa4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57aa4-108">Remarks</span></span>

<span data-ttu-id="57aa4-109">Hay problemas importantes que se deben tener en cuenta antes de decidir el método para calcular las referencias del código.</span><span class="sxs-lookup"><span data-stu-id="57aa4-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="57aa4-110">Estos problemas están relacionados con el tamaño y el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="57aa4-110">These issues concern size and performance.</span></span> <span data-ttu-id="57aa4-111">El compilador MIDL proporciona dos métodos para calcular las referencias del código: modo mixto (**/os**) y totalmente interpretado ([**/OI**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="57aa4-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="57aa4-112">El método totalmente interpretado calcula las referencias de los datos completamente sin conexión.</span><span class="sxs-lookup"><span data-stu-id="57aa4-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="57aa4-113">Esto reduce considerablemente el tamaño del código auxiliar, pero también reduce el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="57aa4-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="57aa4-114">Use el modo predeterminado de MIDL **/Oicf** /Robust para todos los fines distintos de la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="57aa4-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="57aa4-115">Este modo es el modo estándar seguro del compilador MIDL; cualquier otro modo se debe usar solo después de haber tenido cuidado en la implicación de la seguridad, de modo que las extensiones futuras solo se implementarán para el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="57aa4-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="57aa4-116">En el modo mixto, el compilador calcula las referencias de algunos parámetros insertados en el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="57aa4-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="57aa4-117">Aunque esto da como resultado un mayor tamaño de código auxiliar, también puede ofrecer mayor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="57aa4-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="57aa4-118">MIDL proporciona compatibilidad total con las matrices multidimensionales y los punteros de tamaño multidimensional solo en modo [**/Oicf**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="57aa4-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="57aa4-119">En los modos **/os** y **/OI** , el compilador admite casos sencillos, como matrices de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="57aa4-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="57aa4-120">El uso de matrices multidimensionales en los modos **/os** o **/OI** puede dar lugar a parámetros cuyas referencias no se han calculado correctamente.</span><span class="sxs-lookup"><span data-stu-id="57aa4-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="57aa4-121">Microsoft recomienda que use el modificador de la línea de comandos **/Oicf** cuando la interfaz defina parámetros que son matrices multidimensionales o punteros de tamaño multidimensional.</span><span class="sxs-lookup"><span data-stu-id="57aa4-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="57aa4-122">Para definir con mayor precisión el nivel de degradado en la forma en que se calculan las referencias de los datos, esta versión de RPC proporciona un \[ atributo [**Optimize**](optimize.md) \] .</span><span class="sxs-lookup"><span data-stu-id="57aa4-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="57aa4-123">Este atributo se usa como atributo de interfaz ACF u operación para seleccionar el modo de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="57aa4-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="57aa4-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="57aa4-124">Examples</span></span>

<span data-ttu-id="57aa4-125">**MIDL/os FILENAME. idl**</span><span class="sxs-lookup"><span data-stu-id="57aa4-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="57aa4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="57aa4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aa4-127">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="57aa4-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="57aa4-128">**/OI**</span><span class="sxs-lookup"><span data-stu-id="57aa4-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="57aa4-129">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="57aa4-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="57aa4-130">**/no \_ format \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="57aa4-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




