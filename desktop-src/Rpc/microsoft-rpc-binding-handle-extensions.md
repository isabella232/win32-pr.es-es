---
title: Extensiones de Binding-Handle de Microsoft RPC
description: Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro, más a la izquierda.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078515"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="3a724-103">Extensiones de Binding-Handle de Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="3a724-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="3a724-104">Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro, más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="3a724-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="3a724-105">En los pasos siguientes se describe la secuencia con la que pasa el compilador de MIDL para resolver el parámetro de identificador de enlace en modo de compatibilidad de DCE (/**OSF**) y en modo predeterminado (Microsoft-Extended).</span><span class="sxs-lookup"><span data-stu-id="3a724-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="3a724-106">Modo de compatibilidad de DCE</span><span class="sxs-lookup"><span data-stu-id="3a724-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="3a724-107">Identificador de enlace que aparece en la primera posición.</span><span class="sxs-lookup"><span data-stu-id="3a724-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="3a724-108">El \[ parámetro de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) [**en**](/windows/desktop/Midl/in)el extremo izquierdo \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="3a724-109">Identificador de enlace implícito especificado por el identificador \[ [**implícito \_**](/windows/desktop/Midl/implicit-handle) \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="3a724-110">Si no hay ningún ACF presente, el valor predeterminado es usar el \[ **\_ controlador automático** \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="3a724-111">Modo predeterminado</span><span class="sxs-lookup"><span data-stu-id="3a724-111">Default mode</span></span>

-   <span data-ttu-id="3a724-112">Identificador de enlace explícito más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="3a724-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="3a724-113">Identificador de enlace implícito especificado por el identificador \[ [**implícito \_**](/windows/desktop/Midl/implicit-handle) \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="3a724-114">Si no hay ningún ACF presente, el valor predeterminado es usar el \[ [**\_ controlador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="3a724-115">Los compiladores de DCE IDL buscan un identificador de enlace explícito como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3a724-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="3a724-116">Cuando el primer parámetro no es un identificador de enlace y se especifican uno o más identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="3a724-117">Cuando el primer parámetro no es un identificador y no hay identificadores de contexto, el procedimiento utiliza el enlace implícito mediante el \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del atributo ACF \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="3a724-118">Las extensiones de Microsoft para el IDL permiten que el controlador de enlace esté en una posición distinta del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3a724-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="3a724-119">El extremo izquierdo \[ [**en**](/windows/desktop/Midl/in) el \] parámetro de identificador explícito, ya sea un identificador primitivo, definido por el programador o el contexto, es el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="3a724-120">Cuando no hay ningún parámetro de identificador, el procedimiento utiliza el enlace implícito mediante el \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del atributo ACF \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="3a724-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="3a724-121">Las siguientes reglas se aplican al modo de compatibilidad con DCE (/OSF) y al modo predeterminado:</span><span class="sxs-lookup"><span data-stu-id="3a724-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="3a724-122">El enlace de control automático se utiliza cuando no hay ACF.</span><span class="sxs-lookup"><span data-stu-id="3a724-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="3a724-123">\[ [](/windows/desktop/Midl/in) \] \[ Los identificadores [**out**](/windows/desktop/Midl/out-idl) in o **in**, out explícitos \] para una función individual tienen preferencia sobre cualquier enlace implícito especificado para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3a724-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="3a724-124">\[ [](/windows/desktop/Midl/in) \] \[  \] No se admiten varios identificadores primitivos en o en.</span><span class="sxs-lookup"><span data-stu-id="3a724-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="3a724-125">\[ [](/windows/desktop/Midl/in) \] \[  \] Se permiten varios identificadores de contexto explícitos en o en.</span><span class="sxs-lookup"><span data-stu-id="3a724-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="3a724-126">Todos los parámetros de identificador definidos por el programador, excepto el parámetro de identificador de enlace, se tratan como datos transmisibles.</span><span class="sxs-lookup"><span data-stu-id="3a724-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="3a724-127">La tabla siguiente contiene ejemplos y describe cómo se asignan los identificadores de enlace en cada modo del compilador.</span><span class="sxs-lookup"><span data-stu-id="3a724-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3a724-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a724-128">Example</span></span></th>
<th><span data-ttu-id="3a724-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a724-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="3a724-130">No se especifica ningún identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="3a724-130">No explicit handle is specified.</span></span> <span data-ttu-id="3a724-131">Se utiliza el identificador de enlace implícito, especificado por [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>].</span><span class="sxs-lookup"><span data-stu-id="3a724-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="3a724-132">Cuando no hay ACF, se usa un identificador automático.</span><span class="sxs-lookup"><span data-stu-id="3a724-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="3a724-133">Se especifica un identificador explícito de tipo handle_t.</span><span class="sxs-lookup"><span data-stu-id="3a724-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="3a724-134">El parámetro <em>H</em> es el identificador de enlace para el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="3a724-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="3a724-135">El primer parámetro no es un identificador.</span><span class="sxs-lookup"><span data-stu-id="3a724-135">The first parameter is not a handle.</span></span> <span data-ttu-id="3a724-136">En el modo predeterminado, el parámetro de identificador de la izquierda, <em>H</em>, es el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="3a724-137">En modo/OSF, se usa el enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="3a724-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="3a724-138">Se ha detectado un error porque se espera que el segundo parámetro sea transmisible y handle_t no se puede transmitir.</span><span class="sxs-lookup"><span data-stu-id="3a724-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="3a724-139">El primer parámetro no es un identificador.</span><span class="sxs-lookup"><span data-stu-id="3a724-139">The first parameter is not a handle.</span></span> <span data-ttu-id="3a724-140">En el modo predeterminado, el parámetro de identificador de la izquierda, <em>H</em>, es el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="3a724-141">El código auxiliar llama a las rutinas proporcionadas por el usuario MY_HDL_bind y MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="3a724-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="3a724-142">En el modo/OSF, se usa el enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="3a724-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="3a724-143">El parámetro de identificador definido por el programador <em>H</em> se trata como datos transmisibles.</span><span class="sxs-lookup"><span data-stu-id="3a724-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="3a724-144">El primer parámetro es un identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="3a724-145">El parámetro <em>H</em> es el parámetro de identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="3a724-146">El segundo parámetro de identificador definido por el programador se trata como datos transmisibles.</span><span class="sxs-lookup"><span data-stu-id="3a724-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="3a724-147">El identificador de enlace es un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="3a724-147">The binding handle is a context handle.</span></span> <span data-ttu-id="3a724-148">El parámetro <em>H</em> es el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="3a724-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 