---
title: API DE WFP
description: La API de la plataforma de filtrado de Windows (WFP) se divide en los siguientes componentes.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105685808"
---
# <a name="wfp-api"></a><span data-ttu-id="8c791-103">API DE WFP</span><span class="sxs-lookup"><span data-stu-id="8c791-103">WFP API</span></span>

<span data-ttu-id="8c791-104">La API de la plataforma de filtrado de Windows (WFP) se divide en los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="8c791-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c791-105">Componente</span><span class="sxs-lookup"><span data-stu-id="8c791-105">Component</span></span></th>
<th><span data-ttu-id="8c791-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c791-106">Description</span></span></th>
<th><span data-ttu-id="8c791-107">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c791-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="8c791-108"><a href="/windows-hardware/drivers/ddi/_netvista/">CALLOUT API</a> (FWPS) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8c791-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8c791-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Tipos de datos</a> usados por las llamadas. <strong>Nota:</strong>  Estos tipos de datos se documentan en el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8c791-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="8c791-110">fwpstypes. h</span><span class="sxs-lookup"><span data-stu-id="8c791-110">fwpstypes.h</span></span><br />
<span data-ttu-id="8c791-111">fwpstypes. idl</span><span class="sxs-lookup"><span data-stu-id="8c791-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c791-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Funciones</a> y <a href="/windows-hardware/drivers/ddi/_netvista/">tipos enumerados</a> que se usan para implementar llamadas. <strong>Nota:</strong>  Estas funciones y tipos enumerados se documentan en el DDK.</span><span class="sxs-lookup"><span data-stu-id="8c791-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="8c791-113">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-113">fwpsu.h</span></span><br />
<span data-ttu-id="8c791-114">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="8c791-115">API de IKE/AuthIP (IKEEXT) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8c791-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8c791-116">Tipos y <a href="fwp-structs.md">estructuras</a> <a href="fwp-enums.md">enumerados</a> utilizados para administrar las asociaciones de seguridad y directivas de modo principal de IKE y AuthIP (mm).</span><span class="sxs-lookup"><span data-stu-id="8c791-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="8c791-117">iketypes. h</span><span class="sxs-lookup"><span data-stu-id="8c791-117">iketypes.h</span></span><br />
<span data-ttu-id="8c791-118">iketypes. idl</span><span class="sxs-lookup"><span data-stu-id="8c791-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c791-119"><a href="fwp-ike-functions.md">Funciones</a> que se usan para administrar las asociaciones de seguridad y directivas de IKE y AuthIP mm.</span><span class="sxs-lookup"><span data-stu-id="8c791-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="8c791-120">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-120">fwpmu.h</span></span><br />
<span data-ttu-id="8c791-121">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="8c791-122">IPsec API (IPSEC) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8c791-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8c791-123">Tipos y <a href="fwp-structs.md">estructuras</a> <a href="fwp-enums.md">enumerados</a> utilizados para administrar directivas IPSec y asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c791-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="8c791-124">ipsectypes. h</span><span class="sxs-lookup"><span data-stu-id="8c791-124">ipsectypes.h</span></span><br />
<span data-ttu-id="8c791-125">ipsectypes. idl</span><span class="sxs-lookup"><span data-stu-id="8c791-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c791-126"><a href="fwp-ipsec-functions.md">Funciones</a> que se usan para administrar directivas IPSec y asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c791-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="8c791-127">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-127">fwpmu.h</span></span><br />
<span data-ttu-id="8c791-128">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="8c791-129">API de administración (FWPM) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8c791-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8c791-130"><a href="fwp-enums.md">Tipos enumerados</a> y <a href="fwp-structs.md">estructuras</a> que se usan para administrar el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="8c791-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="8c791-131">fwpmtypes. h</span><span class="sxs-lookup"><span data-stu-id="8c791-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="8c791-132">fwpmtypes. idl</span><span class="sxs-lookup"><span data-stu-id="8c791-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c791-133"><a href="fwp-mgmt-functions.md">Funciones</a> utilizadas para administrar el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="8c791-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="8c791-134">Estas funciones se utilizan para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="8c791-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="8c791-135">Establecer y consultar filtros, proveedores y llamadas.</span><span class="sxs-lookup"><span data-stu-id="8c791-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="8c791-136">Recuperar estadísticas de IPsec.</span><span class="sxs-lookup"><span data-stu-id="8c791-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="8c791-137">Configure la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="8c791-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="8c791-138">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-138">fwpmu.h</span></span><br />
<span data-ttu-id="8c791-139">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8c791-140">API compartida (FWP)</span><span class="sxs-lookup"><span data-stu-id="8c791-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="8c791-141">Tipos y <a href="fwp-structs.md">estructuras</a> fundamentales <a href="fwp-enums.md">enumerados</a> compartidos por la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="8c791-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="8c791-142">fwptypes. h</span><span class="sxs-lookup"><span data-stu-id="8c791-142">fwptypes.h</span></span><br />
<span data-ttu-id="8c791-143">fwptypes. idl</span><span class="sxs-lookup"><span data-stu-id="8c791-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8c791-144">Los nombres de los tipos de datos se encuentran en mayúsculas y con un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="8c791-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="8c791-145">El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="8c791-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="8c791-146">Los nombres de función se mezclan en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8c791-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="8c791-147">El nombre siempre comienza con un prefijo que identifica su grupo de componentes, como [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="8c791-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="8c791-148">La mayoría de los nombres de datos y de funciones terminan con un número de versión.</span><span class="sxs-lookup"><span data-stu-id="8c791-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="8c791-149">El archivo de encabezado fwpvi. h asigna los nombres de función y datos independientes de la versión a la versión que es adecuada para su uso con un sistema operativo determinado.</span><span class="sxs-lookup"><span data-stu-id="8c791-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="8c791-150">Para obtener más información, consulte [los nombres de Version-Independent de WFP y el destino de versiones específicas de Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="8c791-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="8c791-151">Cada componente no es independiente.</span><span class="sxs-lookup"><span data-stu-id="8c791-151">Each component does not stand alone.</span></span> <span data-ttu-id="8c791-152">Por ejemplo, las directivas de modo principal IKE (MM) se definen en el componente IKEEXT, pero se almacenan en un contexto de proveedor y se asocian con un filtro que se encuentran en el componente de la API FWPM.</span><span class="sxs-lookup"><span data-stu-id="8c791-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="8c791-153">User-Mode y Kernel-Mode archivos de encabezado públicos</span><span class="sxs-lookup"><span data-stu-id="8c791-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="8c791-154">La mayoría de las funciones de WFP se pueden llamar desde el modo de usuario o el modo kernel.</span><span class="sxs-lookup"><span data-stu-id="8c791-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="8c791-155">Sin embargo, las funciones de modo de usuario devuelven un valor **DWORD** que representa un código de error de Win32, mientras que las funciones de modo kernel devuelven un valor de **NTSTATUS** que representa un código de estado de NT.</span><span class="sxs-lookup"><span data-stu-id="8c791-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="8c791-156">Como resultado, los nombres de función y la semántica son idénticos entre el modo de usuario y el modo kernel, pero no las signaturas de función.</span><span class="sxs-lookup"><span data-stu-id="8c791-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="8c791-157">Esto requiere encabezados específicos en modo de usuario y en modo kernel para los prototipos de función.</span><span class="sxs-lookup"><span data-stu-id="8c791-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="8c791-158">Los nombres de archivo de encabezado de modo de usuario terminan en "u" y los nombres de archivo de encabezado de modo kernel terminan en "k".</span><span class="sxs-lookup"><span data-stu-id="8c791-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="8c791-159">En la tabla siguiente se enumeran los archivos de encabezado Win32 que definen las funciones de WFP.</span><span class="sxs-lookup"><span data-stu-id="8c791-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="8c791-160">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8c791-160">Header Files</span></span> | <span data-ttu-id="8c791-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c791-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c791-162">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-162">fwpmk.h</span></span>      | <span data-ttu-id="8c791-163">Prototipos de función de modo kernel para los componentes FWPM, IPsec y IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="8c791-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="8c791-164">Solo está disponible en el DDK.</span><span class="sxs-lookup"><span data-stu-id="8c791-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8c791-165">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-165">fwpmu.h</span></span>      | <span data-ttu-id="8c791-166">Prototipos de función de modo de usuario para los componentes FWPM, IPsec y IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="8c791-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="8c791-167">Solo disponible en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8c791-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8c791-168">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="8c791-168">fwpsk.h</span></span>      | <span data-ttu-id="8c791-169">Prototipos de función de modo kernel y tipos enumerados para el componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="8c791-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="8c791-170">Solo está disponible en el DDK.</span><span class="sxs-lookup"><span data-stu-id="8c791-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8c791-171">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="8c791-171">fwpsu.h</span></span>      | <span data-ttu-id="8c791-172">Prototipos de función de modo de usuario y tipos enumerados para el componente FWPS.</span><span class="sxs-lookup"><span data-stu-id="8c791-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="8c791-173">Solo está disponible en el Windows SDK. **Nota:**  Los tipos enumerados de modo de usuario FWPS son idénticos a los tipos enumerados de FWPS de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="8c791-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="8c791-174">En consecuencia, estos tipos se documentan solo en el DDK.</span><span class="sxs-lookup"><span data-stu-id="8c791-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="8c791-175">**Nota:**  Los prototipos de función FWPS de modo usuario son idénticos a los prototipos de función FWPS de modo kernel con la excepción del código de retorno.</span><span class="sxs-lookup"><span data-stu-id="8c791-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="8c791-176">Las funciones FWPS de modo usuario devuelven un **valor DWORD**, mientras que las funciones FWPS de modo kernel devuelven un **NTSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="8c791-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="8c791-177">En consecuencia, estas funciones solo se documentan en el DDK.</span><span class="sxs-lookup"><span data-stu-id="8c791-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="8c791-178">Todas las funciones de modo de usuario se exportan desde fwpuclnt.dll.</span><span class="sxs-lookup"><span data-stu-id="8c791-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="8c791-179">Todas las funciones de modo kernel se exportan desde fwpkclnt.sys.</span><span class="sxs-lookup"><span data-stu-id="8c791-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="8c791-180">Tipos de datos Management (FWPM) y Callout (FWPS)</span><span class="sxs-lookup"><span data-stu-id="8c791-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="8c791-181">La mayoría de los tipos de datos FWPM, que se usan para tareas de administración como agregar filtros o llamadas desde una aplicación o un controlador, tienen homólogos FWPS.</span><span class="sxs-lookup"><span data-stu-id="8c791-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="8c791-182">Los tipos de datos FWPS se usan durante el filtrado real del tráfico de red, en el contexto de una rutina de llamada para la clasificación.</span><span class="sxs-lookup"><span data-stu-id="8c791-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="8c791-183">Por ejemplo, para agregar un filtro a una capa determinada del motor de filtrado, el programador debe usar un tipo FWPM, como: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` .</span><span class="sxs-lookup"><span data-stu-id="8c791-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="8c791-184">Para comprobar a qué capa se llama una llamada, el programador debe usar el tipo de FWPS correspondiente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="8c791-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="8c791-185">Algunos homólogos de FWPS para tipos de datos de FWPM están expandiendo los tipos de datos FWPM originales.</span><span class="sxs-lookup"><span data-stu-id="8c791-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="8c791-186">Por ejemplo, para agregar una condición de filtro en muchas capas del motor de filtrado, el programador especifica `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` independientemente de la capa del motor de filtrado.</span><span class="sxs-lookup"><span data-stu-id="8c791-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="8c791-187">Para buscar un valor de condición de filtro, el programador especifica un tipo de FWPS específico de la capa, como: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .</span><span class="sxs-lookup"><span data-stu-id="8c791-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="8c791-188">Los tipos de datos FWPS suelen ser más pequeños que sus homólogos FWPM.</span><span class="sxs-lookup"><span data-stu-id="8c791-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="8c791-189">Por ejemplo, los [**identificadores de nivel de filtrado de FWPM**](management-filtering-layer-identifiers-.md) son **GUID** s (16 bytes), mientras que los [identificadores de nivel de filtrado de FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) son **UINT16** (16 bits).</span><span class="sxs-lookup"><span data-stu-id="8c791-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="8c791-190">El tamaño más pequeño de los tipos de datos FWPS mejora el rendimiento del sistema, ya que las comparaciones de enteros compensan las comparaciones de **GUID** para el tráfico en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8c791-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="8c791-191">Además, la memoria del kernel se utiliza de forma eficaz, ya que todos los tipos de FWPS se usan en el kernel para administrar los filtros, mientras que los tipos de FWPM se almacenan en modo de usuario para administrar los distintos niveles.</span><span class="sxs-lookup"><span data-stu-id="8c791-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c791-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c791-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c791-193">Modelo de objetos de API de WFP</span><span class="sxs-lookup"><span data-stu-id="8c791-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="8c791-194">Administración de objetos de API de WFP</span><span class="sxs-lookup"><span data-stu-id="8c791-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

