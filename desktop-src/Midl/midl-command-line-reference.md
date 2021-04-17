---
title: Referencia de Command-Line de MIDL
description: Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador que reconoce el compilador de MIDL de Microsoft RPC.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, referencia
- referencia de la línea de comandos MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105666095"
---
# <a name="midl-command-line-reference"></a><span data-ttu-id="a49c2-105">Referencia de Command-Line de MIDL</span><span class="sxs-lookup"><span data-stu-id="a49c2-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="a49c2-106">Esta sección contiene información de referencia para cada modificador de línea de comandos y opción de modificador que reconoce el compilador de MIDL de Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="a49c2-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="a49c2-107">Las entradas de conmutador están organizadas en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="a49c2-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="a49c2-108">La [Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md) describe la sintaxis de línea de comandos general.</span><span class="sxs-lookup"><span data-stu-id="a49c2-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="a49c2-109">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="a49c2-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="a49c2-110">Comando de archivo de respuesta</span><span class="sxs-lookup"><span data-stu-id="a49c2-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="a49c2-111">**/acf**</span><span class="sxs-lookup"><span data-stu-id="a49c2-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="a49c2-112">**especific**</span><span class="sxs-lookup"><span data-stu-id="a49c2-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="a49c2-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="a49c2-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="a49c2-114">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="a49c2-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="a49c2-115">compatibilidad con/backward \_</span><span class="sxs-lookup"><span data-stu-id="a49c2-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="a49c2-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="a49c2-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="a49c2-117">**/caux**</span><span class="sxs-lookup"><span data-stu-id="a49c2-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="a49c2-118">**/Char**</span><span class="sxs-lookup"><span data-stu-id="a49c2-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="a49c2-119">**/Client**</span><span class="sxs-lookup"><span data-stu-id="a49c2-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="a49c2-120">**/confirm**</span><span class="sxs-lookup"><span data-stu-id="a49c2-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="a49c2-121">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="a49c2-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="a49c2-122">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="a49c2-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="a49c2-123">[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="a49c2-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="a49c2-124">**/D.**</span><span class="sxs-lookup"><span data-stu-id="a49c2-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="a49c2-125">**/dlldata**</span><span class="sxs-lookup"><span data-stu-id="a49c2-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="a49c2-126">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="a49c2-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="a49c2-127">**/error**</span><span class="sxs-lookup"><span data-stu-id="a49c2-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="a49c2-128">**/error**</span><span class="sxs-lookup"><span data-stu-id="a49c2-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="a49c2-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="a49c2-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="a49c2-130">**/header**</span><span class="sxs-lookup"><span data-stu-id="a49c2-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="a49c2-131">**/Help (/?)**</span><span class="sxs-lookup"><span data-stu-id="a49c2-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="a49c2-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="a49c2-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="a49c2-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="a49c2-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="a49c2-134">**/IID**</span><span class="sxs-lookup"><span data-stu-id="a49c2-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="a49c2-135">**/Import**</span><span class="sxs-lookup"><span data-stu-id="a49c2-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="a49c2-136">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="a49c2-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="a49c2-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="a49c2-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="a49c2-138">**\_ext/MS**</span><span class="sxs-lookup"><span data-stu-id="a49c2-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="a49c2-139">**\_Unión/MS**</span><span class="sxs-lookup"><span data-stu-id="a49c2-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="a49c2-140">**/MSC \_ ver**</span><span class="sxs-lookup"><span data-stu-id="a49c2-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="a49c2-141">**/pedidos nuevos**</span><span class="sxs-lookup"><span data-stu-id="a49c2-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="a49c2-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="a49c2-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="a49c2-143">**/no \_ CPP,/nocpp**</span><span class="sxs-lookup"><span data-stu-id="a49c2-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="a49c2-144">**/no \_ default \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="a49c2-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="a49c2-145">**/no \_ Def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="a49c2-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="a49c2-146">**/no \_ format \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="a49c2-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="a49c2-147">**/no \_ robusto**</span><span class="sxs-lookup"><span data-stu-id="a49c2-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="a49c2-148">**/no \_ WARN**</span><span class="sxs-lookup"><span data-stu-id="a49c2-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="a49c2-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="a49c2-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="a49c2-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="a49c2-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="a49c2-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="a49c2-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="a49c2-152">**/OI**</span><span class="sxs-lookup"><span data-stu-id="a49c2-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="a49c2-153">**/Old**</span><span class="sxs-lookup"><span data-stu-id="a49c2-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="a49c2-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="a49c2-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="a49c2-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="a49c2-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="a49c2-156">**/Os**</span><span class="sxs-lookup"><span data-stu-id="a49c2-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="a49c2-157">**/osf**</span><span class="sxs-lookup"><span data-stu-id="a49c2-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="a49c2-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="a49c2-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="a49c2-159">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="a49c2-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="a49c2-160">**/prefix**</span><span class="sxs-lookup"><span data-stu-id="a49c2-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="a49c2-161">**/Protocolo**</span><span class="sxs-lookup"><span data-stu-id="a49c2-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="a49c2-162">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="a49c2-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="a49c2-163">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="a49c2-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="a49c2-164">**/rpcss**</span><span class="sxs-lookup"><span data-stu-id="a49c2-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="a49c2-165">**/sal**</span><span class="sxs-lookup"><span data-stu-id="a49c2-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="a49c2-166">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="a49c2-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="a49c2-167">**/saux**</span><span class="sxs-lookup"><span data-stu-id="a49c2-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="a49c2-168">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="a49c2-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="a49c2-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="a49c2-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="a49c2-170">**comprobación de/Syntax \_**</span><span class="sxs-lookup"><span data-stu-id="a49c2-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="a49c2-171">**/Target**</span><span class="sxs-lookup"><span data-stu-id="a49c2-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="a49c2-172">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="a49c2-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="a49c2-173">**/U**</span><span class="sxs-lookup"><span data-stu-id="a49c2-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="a49c2-174">**/Use \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="a49c2-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="a49c2-175">**\_marca/version**</span><span class="sxs-lookup"><span data-stu-id="a49c2-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="a49c2-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="a49c2-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="a49c2-177">**/WARN**</span><span class="sxs-lookup"><span data-stu-id="a49c2-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="a49c2-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="a49c2-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="a49c2-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="a49c2-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="a49c2-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="a49c2-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="a49c2-181">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="a49c2-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="a49c2-182">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="a49c2-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="a49c2-183">El compilador MIDL puede generar código para distintas plataformas y versiones del sistema.</span><span class="sxs-lookup"><span data-stu-id="a49c2-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="a49c2-184">Consulte el modificador [**/target**](-target.md) para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.</span><span class="sxs-lookup"><span data-stu-id="a49c2-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="a49c2-185">Tenga en cuenta que el signo menos (–) se puede sustituir por la barra diagonal (/) en todos los modificadores de la línea de comandos de MIDL que comienzan por una barra diagonal (/).</span><span class="sxs-lookup"><span data-stu-id="a49c2-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="a49c2-186">En el ejemplo siguiente se muestra su equivalencia al invocar el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a49c2-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="a49c2-187">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a49c2-187">Examples</span></span>

<span data-ttu-id="a49c2-188">**MIDL/ACF My \_ ACF. ACF** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="a49c2-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="a49c2-189">**MIDL-ACF My \_ ACF. ACF** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="a49c2-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 




