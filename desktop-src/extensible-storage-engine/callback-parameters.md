---
description: 'Más información sobre: parámetros de devolución de llamada'
title: Parámetros de devolución de llamada
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155057"
---
# <a name="callback-parameters"></a><span data-ttu-id="b075e-103">Parámetros de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="b075e-103">Callback Parameters</span></span>


<span data-ttu-id="b075e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b075e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="b075e-105">Parámetros de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="b075e-105">Callback Parameters</span></span>

<span data-ttu-id="b075e-106">Este tema contiene los parámetros que se utilizan para las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="b075e-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="b075e-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="b075e-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="b075e-108">65</span><span class="sxs-lookup"><span data-stu-id="b075e-108">65</span></span>  

<span data-ttu-id="b075e-109">Este parámetro deshabilita todas las devoluciones de llamada del motor de base de datos en funciones proporcionadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b075e-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="b075e-110">Está pensado principalmente para admitir las utilidades del motor de base de datos y no está diseñado para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b075e-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b075e-111">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b075e-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b075e-112">False</span><span class="sxs-lookup"><span data-stu-id="b075e-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b075e-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="b075e-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="b075e-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b075e-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b075e-116">False, True</span><span class="sxs-lookup"><span data-stu-id="b075e-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-117">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b075e-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b075e-118">Instancia</span><span class="sxs-lookup"><span data-stu-id="b075e-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-119">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-120">Sí</span><span class="sxs-lookup"><span data-stu-id="b075e-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-121">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-122">No</span><span class="sxs-lookup"><span data-stu-id="b075e-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-123">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b075e-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b075e-124">No</span><span class="sxs-lookup"><span data-stu-id="b075e-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-125">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-126">No</span><span class="sxs-lookup"><span data-stu-id="b075e-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-127">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b075e-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b075e-128">No</span><span class="sxs-lookup"><span data-stu-id="b075e-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-129">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b075e-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b075e-130">No</span><span class="sxs-lookup"><span data-stu-id="b075e-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-131">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-132">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b075e-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b075e-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="b075e-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="b075e-134">156</span><span class="sxs-lookup"><span data-stu-id="b075e-134">156</span></span>  

<span data-ttu-id="b075e-135">Este parámetro habilita el uso de devoluciones de llamada persistentes en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b075e-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="b075e-136">En las versiones anteriores a Windows Vista, el uso de las devoluciones de llamada persistentes estaba habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b075e-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="b075e-137">Ahora, las aplicaciones deben habilitar explícitamente el uso de devoluciones de llamada persistentes en tiempo de ejecución con este parámetro.</span><span class="sxs-lookup"><span data-stu-id="b075e-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="b075e-138">Si no se establece este parámetro, se producirá un error en cualquier operación de base de datos que requiera la invocación de una devolución de llamada con JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="b075e-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="b075e-139">Este parámetro no afecta a las devoluciones de llamada que se especifican en tiempo de ejecución con los mecanismos siguientes: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)o un parámetro de devolución de llamada explícito a una API de jet.</span><span class="sxs-lookup"><span data-stu-id="b075e-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="b075e-140">Todavía es posible crear elementos de esquema que contengan devoluciones de llamada persistentes aunque no se permita el uso de esas devoluciones de llamada persistentes.</span><span class="sxs-lookup"><span data-stu-id="b075e-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="b075e-141">Cuando este parámetro se establece en false, invalida JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="b075e-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b075e-142">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b075e-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b075e-143">False</span><span class="sxs-lookup"><span data-stu-id="b075e-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-144">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b075e-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="b075e-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="b075e-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-146">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b075e-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b075e-147">False, True</span><span class="sxs-lookup"><span data-stu-id="b075e-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-148">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b075e-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b075e-149">Instancia</span><span class="sxs-lookup"><span data-stu-id="b075e-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-150">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-151">Sí</span><span class="sxs-lookup"><span data-stu-id="b075e-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-152">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-153">No</span><span class="sxs-lookup"><span data-stu-id="b075e-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-154">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b075e-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b075e-155">No</span><span class="sxs-lookup"><span data-stu-id="b075e-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-156">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-157">No</span><span class="sxs-lookup"><span data-stu-id="b075e-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-158">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b075e-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b075e-159">No</span><span class="sxs-lookup"><span data-stu-id="b075e-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-160">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b075e-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b075e-161">No</span><span class="sxs-lookup"><span data-stu-id="b075e-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-162">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-163">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b075e-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b075e-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="b075e-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="b075e-165">73</span><span class="sxs-lookup"><span data-stu-id="b075e-165">73</span></span>  

<span data-ttu-id="b075e-166">Este parámetro configura el motor con una función de devolución de llamada en tiempo de ejecución que implementa la interfaz [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b075e-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="b075e-167">Se puede llamar a esta devolución de llamada por los siguientes motivos: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)o [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="b075e-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="b075e-168">Consulte [JetSetLS](./jetsetls-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b075e-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b075e-169">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b075e-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b075e-170">NULL</span><span class="sxs-lookup"><span data-stu-id="b075e-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-171">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b075e-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="b075e-172">Puntero a función (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="b075e-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b075e-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b075e-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="b075e-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-175">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b075e-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b075e-176">Instancia</span><span class="sxs-lookup"><span data-stu-id="b075e-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-177">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-178">Sí</span><span class="sxs-lookup"><span data-stu-id="b075e-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-179">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b075e-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b075e-180">No</span><span class="sxs-lookup"><span data-stu-id="b075e-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-181">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b075e-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b075e-182">No</span><span class="sxs-lookup"><span data-stu-id="b075e-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-183">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-184">No</span><span class="sxs-lookup"><span data-stu-id="b075e-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-185">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b075e-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b075e-186">No</span><span class="sxs-lookup"><span data-stu-id="b075e-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-187">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b075e-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b075e-188">No</span><span class="sxs-lookup"><span data-stu-id="b075e-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-189">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b075e-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b075e-190">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b075e-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="b075e-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b075e-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b075e-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b075e-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b075e-193">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b075e-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b075e-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b075e-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b075e-195">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b075e-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b075e-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b075e-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b075e-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b075e-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b075e-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b075e-198">See Also</span></span>

[<span data-ttu-id="b075e-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="b075e-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="b075e-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="b075e-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="b075e-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="b075e-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="b075e-202">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b075e-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b075e-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="b075e-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="b075e-204">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b075e-204">JetSetLS</span></span>](./jetsetls-function.md)
