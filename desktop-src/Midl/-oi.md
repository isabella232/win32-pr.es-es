---
title: Parámetro/OI
description: Los modificadores/OI y/OIC indican al compilador de MIDL que use un método de serialización totalmente interpretado. El modificador/Oicf proporciona mejoras de rendimiento adicionales.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- Parámetro/OI del modificador
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270884"
---
# <a name="oi-switch"></a><span data-ttu-id="57d74-105">Parámetro/OI</span><span class="sxs-lookup"><span data-stu-id="57d74-105">/Oi switch</span></span>

<span data-ttu-id="57d74-106">Los modificadores **/OI** y **/OIC** indican al compilador de MIDL que use un método de serialización totalmente interpretado.</span><span class="sxs-lookup"><span data-stu-id="57d74-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="57d74-107">El modificador **/Oicf** proporciona mejoras de rendimiento adicionales.</span><span class="sxs-lookup"><span data-stu-id="57d74-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="57d74-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="57d74-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="57d74-109">*OI*</span><span class="sxs-lookup"><span data-stu-id="57d74-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="57d74-110">Especifica el método totalmente interpretado para calcular las referencias del código auxiliar que se pasa entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="57d74-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="57d74-111">Este modificador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="57d74-111">This switch is obsolete.</span></span> <span data-ttu-id="57d74-112">Se recomienda usar el modificador **/Oicf** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="57d74-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="57d74-113">*Oic*</span><span class="sxs-lookup"><span data-stu-id="57d74-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="57d74-114">Especifica el método de serialización del proxy no codificado que proporciona todas las características de **/OI** y, además, reduce aún más el tamaño del código auxiliar de cliente para las interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="57d74-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="57d74-115">Este modificador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="57d74-115">This switch is obsolete.</span></span> <span data-ttu-id="57d74-116">Se recomienda usar el modificador **/Oicf** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="57d74-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="57d74-117">*Interfaces salientes o Oicf*</span><span class="sxs-lookup"><span data-stu-id="57d74-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="57d74-118">Especifica el método de serialización del proxy sin código que incluye todas las características proporcionadas por **/OI** y **/OIC** , pero usa un nuevo intérprete (cadenas de formato rápido) que proporciona un mejor rendimiento que **/OI** o **/OIC**.</span><span class="sxs-lookup"><span data-stu-id="57d74-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="57d74-119">Este modificador incluye mejoras de RPC recientes y se recomienda para escenarios de RPC modernos.</span><span class="sxs-lookup"><span data-stu-id="57d74-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57d74-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57d74-120">Remarks</span></span>

<span data-ttu-id="57d74-121">Tenga en cuenta las restricciones relacionadas con las plataformas de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="57d74-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="57d74-122">El compilador MIDL 3,0 proporciona dos métodos para calcular las referencias del código: interpretado totalmente ( **/OI**, **/OIC** y **/Oicf**) y Mixed-mode ( [**/os**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="57d74-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="57d74-123">A partir de la versión 6.0.359 de MIDL, el compilador MIDL  [**genera código auxiliar**](-robust.md) **/Oicf de** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="57d74-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="57d74-124">Algunas características del lenguaje no se admiten en algunos modos.</span><span class="sxs-lookup"><span data-stu-id="57d74-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="57d74-125">En este caso, el compilador cambia automáticamente al modo apropiado y emite una advertencia.</span><span class="sxs-lookup"><span data-stu-id="57d74-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="57d74-126">Si el rendimiento es un problema, el método de modo mixto ( [**/os**](-os.md)) puede ser el mejor enfoque.</span><span class="sxs-lookup"><span data-stu-id="57d74-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="57d74-127">En este modo, el compilador elige calcular las referencias de algunos parámetros insertados en el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="57d74-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="57d74-128">Aunque esto da como resultado un mayor tamaño de código auxiliar, ofrece un mayor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="57d74-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="57d74-129">El método totalmente interpretado calcula las referencias de los datos completamente sin conexión.</span><span class="sxs-lookup"><span data-stu-id="57d74-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="57d74-130">Esto reduce considerablemente el tamaño del código auxiliar, pero disminuye el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="57d74-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="57d74-131">Además, con el método completamente interpretado, hay un límite de 16 parámetros para cada procedimiento.</span><span class="sxs-lookup"><span data-stu-id="57d74-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="57d74-132">Cualquier procedimiento que contenga más de 16 parámetros se procesará automáticamente en el modo [**/os**](-os.md) .</span><span class="sxs-lookup"><span data-stu-id="57d74-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="57d74-133">Entre los modos interpretados, **/Oicf** ofrece el mejor rendimiento y **/OI** ofrece la mejor compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="57d74-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="57d74-134">Puede usar la opción **/OIF** si la aplicación usa las características de MIDL que se INTRODUJERON con MIDL 3,0, como los atributos de serialización de \[ [**conexión \_**](wire-marshal.md) \] y de cálculo de \[ [**\_ referencias de usuario**](user-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="57d74-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="57d74-135">Si su aplicación usa [canalizaciones](/windows/desktop/Rpc/pipes) , debe usar la opción **/OIF** ; Si especifica otro modo, el compilador MIDL cambiará a **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="57d74-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="57d74-136">Para ajustar la forma en que se calculan las referencias del código auxiliar, Microsoft RPC proporciona un atributo ACF \[ [**Optimize**](optimize.md) \] .</span><span class="sxs-lookup"><span data-stu-id="57d74-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="57d74-137">Este atributo se utiliza como un atributo de interfaz u operación para seleccionar el modo de cálculo de referencias para interfaces individuales o para operaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="57d74-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="57d74-138">Convenciones de llamada</span><span class="sxs-lookup"><span data-stu-id="57d74-138">Calling Conventions</span></span>

<span data-ttu-id="57d74-139">Los códigos auxiliares generados por el compilador MIDL en el método interpretado mediante los modificadores **/OI**, **/OIC** o **/OIF** se deben compilar como un procedimiento Stdcall o Cdecl durante la compilación de C.</span><span class="sxs-lookup"><span data-stu-id="57d74-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="57d74-140">Una Convención de llamada de PASCAL o fastcall no funcionará.</span><span class="sxs-lookup"><span data-stu-id="57d74-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="57d74-141">Además, el código auxiliar del servidor se debe compilar como Stdcall.</span><span class="sxs-lookup"><span data-stu-id="57d74-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="57d74-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="57d74-142">Examples</span></span>

<span data-ttu-id="57d74-143">**nombre de archivo de MIDL/OI. idl**</span><span class="sxs-lookup"><span data-stu-id="57d74-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="57d74-144">**MIDL/OIC nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="57d74-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="57d74-145">**MIDL/OIF nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="57d74-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="57d74-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="57d74-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d74-147">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="57d74-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="57d74-148">**/no \_ robusto**</span><span class="sxs-lookup"><span data-stu-id="57d74-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="57d74-149">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="57d74-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="57d74-150">**/Os**</span><span class="sxs-lookup"><span data-stu-id="57d74-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="57d74-151">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="57d74-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="57d74-152">**/no \_ format \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="57d74-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 