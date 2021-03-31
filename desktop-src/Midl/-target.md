---
title: Modificador /target
description: El modificador/Target permite al compilador MIDL habilitar las optimizaciones disponibles solo en las versiones recientes de Windows. El modificador/Target activa automáticamente modificadores adicionales.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- modificador/Target MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104083522"
---
# <a name="target-switch"></a><span data-ttu-id="d4f10-105">Modificador /target</span><span class="sxs-lookup"><span data-stu-id="d4f10-105">/target switch</span></span>

<span data-ttu-id="d4f10-106">El modificador **/target** permite al compilador MIDL habilitar las optimizaciones disponibles solo en las versiones recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="d4f10-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="d4f10-107">El modificador **/target** activa automáticamente modificadores adicionales.</span><span class="sxs-lookup"><span data-stu-id="d4f10-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="d4f10-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="d4f10-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d4f10-109">*level*</span><span class="sxs-lookup"><span data-stu-id="d4f10-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f10-110">Especifica el nivel de destino, como NT50, NT51, NT60, NT61, NT62 o NT100.</span><span class="sxs-lookup"><span data-stu-id="d4f10-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4f10-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4f10-111">Remarks</span></span>

<span data-ttu-id="d4f10-112">El modificador **/target** activa automáticamente modificadores adicionales, según el sistema operativo, como se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4f10-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="d4f10-113">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d4f10-113">Operating system</span></span> | <span data-ttu-id="d4f10-114">nivel/Target</span><span class="sxs-lookup"><span data-stu-id="d4f10-114">/target level</span></span> | <span data-ttu-id="d4f10-115">Conmutadores activados</span><span class="sxs-lookup"><span data-stu-id="d4f10-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="d4f10-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d4f10-116">Windows 2000</span></span>     | <span data-ttu-id="d4f10-117">NT50</span><span class="sxs-lookup"><span data-stu-id="d4f10-117">NT50</span></span>          | <span data-ttu-id="d4f10-118">/Oicf/error All/Robust</span><span class="sxs-lookup"><span data-stu-id="d4f10-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="d4f10-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4f10-119">Windows XP</span></span>       | <span data-ttu-id="d4f10-120">NT51</span><span class="sxs-lookup"><span data-stu-id="d4f10-120">NT51</span></span>          | <span data-ttu-id="d4f10-121">/Oicf/error All/Robust/protocolo All</span><span class="sxs-lookup"><span data-stu-id="d4f10-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d4f10-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4f10-122">Windows Vista</span></span>    | <span data-ttu-id="d4f10-123">NT60</span><span class="sxs-lookup"><span data-stu-id="d4f10-123">NT60</span></span>          | <span data-ttu-id="d4f10-124">/Oicf/error All/Robust/protocolo All</span><span class="sxs-lookup"><span data-stu-id="d4f10-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d4f10-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4f10-125">Windows 7</span></span>        | <span data-ttu-id="d4f10-126">NT61</span><span class="sxs-lookup"><span data-stu-id="d4f10-126">NT61</span></span>          | <span data-ttu-id="d4f10-127">/Oicf/error All/Robust/protocolo All</span><span class="sxs-lookup"><span data-stu-id="d4f10-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d4f10-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4f10-128">Windows 8</span></span>        | <span data-ttu-id="d4f10-129">NT62</span><span class="sxs-lookup"><span data-stu-id="d4f10-129">NT62</span></span>          | <span data-ttu-id="d4f10-130">/Oicf/error All/Robust/protocolo All</span><span class="sxs-lookup"><span data-stu-id="d4f10-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="d4f10-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4f10-131">Windows 10</span></span>       | <span data-ttu-id="d4f10-132">NT100</span><span class="sxs-lookup"><span data-stu-id="d4f10-132">NT100</span></span>         | <span data-ttu-id="d4f10-133">/Oicf/error All/Robust/protocolo All</span><span class="sxs-lookup"><span data-stu-id="d4f10-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="d4f10-134">Para asegurarse de que un código auxiliar se ejecute en el sistema especificado por el modificador **/target** , MIDL emite un error cuando una característica disponible solo en una versión más reciente de Windows está presente.</span><span class="sxs-lookup"><span data-stu-id="d4f10-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="d4f10-135">En la tabla siguiente se especifica el nivel mínimo de **/target** necesario para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="d4f10-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="d4f10-136">Los niveles de destino más altos incluyen todas las características de los niveles de destino inferiores.</span><span class="sxs-lookup"><span data-stu-id="d4f10-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="d4f10-137">Nivel mínimo necesario de/Target</span><span class="sxs-lookup"><span data-stu-id="d4f10-137">Minimum required /target level</span></span> | <span data-ttu-id="d4f10-138">Características</span><span class="sxs-lookup"><span data-stu-id="d4f10-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f10-139">NT50</span><span class="sxs-lookup"><span data-stu-id="d4f10-139">NT50</span></span>                           | <span data-ttu-id="d4f10-140">/Robust</span><span class="sxs-lookup"><span data-stu-id="d4f10-140">/robust</span></span><br/> <span data-ttu-id="d4f10-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-141">\[message\]</span></span><br/> <span data-ttu-id="d4f10-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-142">\[async\]</span></span><br/> <span data-ttu-id="d4f10-143">\[\_UUID asincrónico\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="d4f10-144">\[notificar \] en modo/Oicf</span><span class="sxs-lookup"><span data-stu-id="d4f10-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="d4f10-145">\[codificar \] o \[ descodificar \] en modo/Oicf</span><span class="sxs-lookup"><span data-stu-id="d4f10-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="d4f10-146">NT51</span><span class="sxs-lookup"><span data-stu-id="d4f10-146">NT51</span></span>                           | <span data-ttu-id="d4f10-147">compatibilidad con/protocolo 64 bits</span><span class="sxs-lookup"><span data-stu-id="d4f10-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="d4f10-148">\[\_omitir parcial\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="d4f10-149">\[forzar \_ asignación\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="d4f10-150">NT60</span><span class="sxs-lookup"><span data-stu-id="d4f10-150">NT60</span></span>                           | <span data-ttu-id="d4f10-151">Serialización de estructura compleja forzada</span><span class="sxs-lookup"><span data-stu-id="d4f10-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="d4f10-152">Identificadores de contexto en una matriz o estructura</span><span class="sxs-lookup"><span data-stu-id="d4f10-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="d4f10-153">\[\]compatibilidad de intervalo para cadenas no de tamaño</span><span class="sxs-lookup"><span data-stu-id="d4f10-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="d4f10-154">\[escribir \_ el \_ identificador de contexto STRICT \_\]</span><span class="sxs-lookup"><span data-stu-id="d4f10-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="d4f10-155">NT61</span><span class="sxs-lookup"><span data-stu-id="d4f10-155">NT61</span></span>                           | <span data-ttu-id="d4f10-156">Las llamadas directas de código auxiliar COM para interfaces con menos de 32 métodos requieren la vinculación de códigos auxiliares COM con **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="d4f10-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="d4f10-157">NT62</span><span class="sxs-lookup"><span data-stu-id="d4f10-157">NT62</span></span>                           | <span data-ttu-id="d4f10-158">Compatibilidad con ARM</span><span class="sxs-lookup"><span data-stu-id="d4f10-158">ARM support</span></span><br/> <span data-ttu-id="d4f10-159">Compatibilidad con WinRT</span><span class="sxs-lookup"><span data-stu-id="d4f10-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="d4f10-160">NT100</span><span class="sxs-lookup"><span data-stu-id="d4f10-160">NT100</span></span>                          | <span data-ttu-id="d4f10-161">\[\]compatibilidad con system_handle</span><span class="sxs-lookup"><span data-stu-id="d4f10-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="d4f10-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4f10-162">Examples</span></span>

<span data-ttu-id="d4f10-163">**MIDL/Target NT50**</span><span class="sxs-lookup"><span data-stu-id="d4f10-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="d4f10-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4f10-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f10-165">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="d4f10-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d4f10-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="d4f10-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
