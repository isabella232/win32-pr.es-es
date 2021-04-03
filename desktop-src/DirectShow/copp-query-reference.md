---
description: Referencia de consulta de COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Referencia de consulta de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080069"
---
# <a name="copp-query-reference"></a><span data-ttu-id="37afd-103">Referencia de consulta de COPP</span><span class="sxs-lookup"><span data-stu-id="37afd-103">COPP Query Reference</span></span>

<span data-ttu-id="37afd-104">En esta sección se describen las consultas de estado admitidas por el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="37afd-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="37afd-105">Para cada consulta, se muestra el GUID que define la consulta, junto con los datos de entrada y los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="37afd-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="37afd-106">Consultar</span><span class="sxs-lookup"><span data-stu-id="37afd-106">Query</span></span>                   | <span data-ttu-id="37afd-107">GUID</span><span class="sxs-lookup"><span data-stu-id="37afd-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="37afd-108">Datos de bus</span><span class="sxs-lookup"><span data-stu-id="37afd-108">Bus Data</span></span>                | <span data-ttu-id="37afd-109">**DXVA \_ COPPQueryBusData**</span><span class="sxs-lookup"><span data-stu-id="37afd-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="37afd-110">Tipo de conector</span><span class="sxs-lookup"><span data-stu-id="37afd-110">Connector Type</span></span>          | <span data-ttu-id="37afd-111">**DXVA \_ COPPQueryConnectorType**</span><span class="sxs-lookup"><span data-stu-id="37afd-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="37afd-112">Mostrar datos</span><span class="sxs-lookup"><span data-stu-id="37afd-112">Display Data</span></span>            | <span data-ttu-id="37afd-113">**DXVA \_ COPPQueryDisplayData**</span><span class="sxs-lookup"><span data-stu-id="37afd-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="37afd-114">Datos de clave de HDCP</span><span class="sxs-lookup"><span data-stu-id="37afd-114">HDCP Key Data</span></span>           | <span data-ttu-id="37afd-115">**DXVA \_ COPPQueryHDCPKeyData**</span><span class="sxs-lookup"><span data-stu-id="37afd-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="37afd-116">Nivel de protección global</span><span class="sxs-lookup"><span data-stu-id="37afd-116">Global Protection Level</span></span> | <span data-ttu-id="37afd-117">**DXVA \_ COPPQueryGlobalProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="37afd-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="37afd-118">Nivel de protección local</span><span class="sxs-lookup"><span data-stu-id="37afd-118">Local Protection Level</span></span>  | <span data-ttu-id="37afd-119">**DXVA \_ COPPQueryLocalProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="37afd-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="37afd-120">Tipo de protección</span><span class="sxs-lookup"><span data-stu-id="37afd-120">Protection Type</span></span>         | <span data-ttu-id="37afd-121">**DXVA \_ COPPQueryProtectionType**</span><span class="sxs-lookup"><span data-stu-id="37afd-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="37afd-122">Signaling</span><span class="sxs-lookup"><span data-stu-id="37afd-122">Signaling</span></span>               | <span data-ttu-id="37afd-123">**DXVA \_ COPPQuerySignaling**</span><span class="sxs-lookup"><span data-stu-id="37afd-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="37afd-124">Consulta de datos de bus</span><span class="sxs-lookup"><span data-stu-id="37afd-124">Bus Data Query</span></span>

<span data-ttu-id="37afd-125">Devuelve el tipo de bus de e/s utilizado por el adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="37afd-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="37afd-126">**GUID**: DXVA \_ COPPQueryBusData</span><span class="sxs-lookup"><span data-stu-id="37afd-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="37afd-127">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-127">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-128">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="37afd-129">El tipo de bus se devuelve en el miembro **dwData** como una marca de la enumeración [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .</span><span class="sxs-lookup"><span data-stu-id="37afd-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="37afd-130">Consulta de tipo de conector</span><span class="sxs-lookup"><span data-stu-id="37afd-130">Connector Type Query</span></span>

<span data-ttu-id="37afd-131">Devuelve el tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="37afd-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="37afd-132">**GUID**: DXVA \_ COPPQueryConnectorType</span><span class="sxs-lookup"><span data-stu-id="37afd-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="37afd-133">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-133">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-134">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="37afd-135">El tipo de conector se devuelve en el miembro **dwData** como una marca de la enumeración [**COPP \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .</span><span class="sxs-lookup"><span data-stu-id="37afd-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="37afd-136">Consulta de visualización de datos</span><span class="sxs-lookup"><span data-stu-id="37afd-136">Display Data Query</span></span>

<span data-ttu-id="37afd-137">Devuelve una descripción de la señal de vídeo que se transmite a través del conector.</span><span class="sxs-lookup"><span data-stu-id="37afd-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="37afd-138">La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de presentación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="37afd-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="37afd-139">Por ejemplo, el modo de presentación del escritorio puede tener 1024x768 píxeles a 85 Hz, mientras que el conector puede ser un conector de S-vídeo que transmite una señal de vídeo a 720 x 480 píxeles, 60/1.01 Hz entrelazada.</span><span class="sxs-lookup"><span data-stu-id="37afd-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="37afd-140">En ese caso, el controlador devolvería la resolución de la señal S-video, no la resolución del escritorio.</span><span class="sxs-lookup"><span data-stu-id="37afd-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="37afd-141">**GUID**: DXVA \_ COPPQueryDisplayData</span><span class="sxs-lookup"><span data-stu-id="37afd-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="37afd-142">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-142">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-143">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="37afd-144">Consulta de datos de clave de HDCP</span><span class="sxs-lookup"><span data-stu-id="37afd-144">HDCP Key Data Query</span></span>

<span data-ttu-id="37afd-145">Devuelve el vector de selección de clave de HDCP del dispositivo (B-KSV).</span><span class="sxs-lookup"><span data-stu-id="37afd-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="37afd-146">KSV es un identificador proporcionado al fabricante del dispositivo y se usa en el proceso de autenticación y configuración de HDCP.</span><span class="sxs-lookup"><span data-stu-id="37afd-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="37afd-147">La aplicación debe comprobar este valor con la lista de KSVs revocados.</span><span class="sxs-lookup"><span data-stu-id="37afd-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="37afd-148">El mecanismo para obtener la lista de revocación de KSV está fuera del ámbito del protocolo COPP.</span><span class="sxs-lookup"><span data-stu-id="37afd-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="37afd-149">Para obtener más información, consulte la especificación de HDCP.</span><span class="sxs-lookup"><span data-stu-id="37afd-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="37afd-150">Esta consulta también determina si el dispositivo HDCP conectado es un monitor o un repetidor de HDCP.</span><span class="sxs-lookup"><span data-stu-id="37afd-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="37afd-151">La aplicación no debe reproducir contenido protegido si el dispositivo HDCP es un repetidor de HDCP, ya que estos no son compatibles con COPP.</span><span class="sxs-lookup"><span data-stu-id="37afd-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="37afd-152">**GUID**: DXVA \_ COPPQueryHDCPKeyData</span><span class="sxs-lookup"><span data-stu-id="37afd-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="37afd-153">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-153">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-154">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="37afd-155">Consulta de nivel de protección global</span><span class="sxs-lookup"><span data-stu-id="37afd-155">Global Protection Level Query</span></span>

<span data-ttu-id="37afd-156">Devuelve el nivel de protección global para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="37afd-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="37afd-157">El nivel de protección global es el nivel de protección que se está aplicando actualmente en el conector, independientemente de cómo se haya indicado al controlador de gráficos que aplique la protección.</span><span class="sxs-lookup"><span data-stu-id="37afd-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="37afd-158">Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la función **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="37afd-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="37afd-159">En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de COPP.</span><span class="sxs-lookup"><span data-stu-id="37afd-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="37afd-160">**GUID**: DXVA \_ COPPQueryGlobalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="37afd-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="37afd-161">**Datos de entrada**: mecanismo de protección que se va a consultar, especificado como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37afd-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="37afd-162">Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="37afd-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="37afd-163">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="37afd-164">El nivel de protección actual se devuelve en el miembro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="37afd-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="37afd-165">El significado de este valor depende del mecanismo de protección que se consulta.</span><span class="sxs-lookup"><span data-stu-id="37afd-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="37afd-166">Para cada mecanismo de protección, el valor del miembro **dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="37afd-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="37afd-167">Mecanismo de protección</span><span class="sxs-lookup"><span data-stu-id="37afd-167">Protection mechanism</span></span> | <span data-ttu-id="37afd-168">Enumeración</span><span class="sxs-lookup"><span data-stu-id="37afd-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="37afd-169">ACP</span><span class="sxs-lookup"><span data-stu-id="37afd-169">ACP</span></span>                  | [<span data-ttu-id="37afd-170">**Nivel de protección de los ACP de COPP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="37afd-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="37afd-171">CGMS-A</span></span>               | [<span data-ttu-id="37afd-172">**Nivel de protección de COPP \_ CGMSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="37afd-173">HDCP</span><span class="sxs-lookup"><span data-stu-id="37afd-173">HDCP</span></span>                 | [<span data-ttu-id="37afd-174">**\_Nivel de \_ protección de HDCP de COPP \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="37afd-175">Consulta de nivel de protección local</span><span class="sxs-lookup"><span data-stu-id="37afd-175">Local Protection Level Query</span></span>

<span data-ttu-id="37afd-176">Devuelve el nivel de protección local para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="37afd-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="37afd-177">El nivel de protección local es el nivel de protección que se solicitó a través de la sesión de COPP actual.</span><span class="sxs-lookup"><span data-stu-id="37afd-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="37afd-178">Es posible que el controlador establezca un nivel de protección superior.</span><span class="sxs-lookup"><span data-stu-id="37afd-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="37afd-179">**GUID**: DXVA \_ COPPQueryLocalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="37afd-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="37afd-180">**Datos de entrada**: mecanismo de protección que se va a consultar, como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37afd-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="37afd-181">Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="37afd-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="37afd-182">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="37afd-183">El nivel de protección actual se devuelve en el miembro **dwData** .</span><span class="sxs-lookup"><span data-stu-id="37afd-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="37afd-184">El significado de este valor depende del mecanismo de protección que se consulta.</span><span class="sxs-lookup"><span data-stu-id="37afd-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="37afd-185">Para cada mecanismo de protección, el valor del miembro **dwData** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="37afd-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="37afd-186">Mecanismo de protección</span><span class="sxs-lookup"><span data-stu-id="37afd-186">Protection mechanism</span></span> | <span data-ttu-id="37afd-187">Enumeración</span><span class="sxs-lookup"><span data-stu-id="37afd-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="37afd-188">ACP</span><span class="sxs-lookup"><span data-stu-id="37afd-188">ACP</span></span>                  | [<span data-ttu-id="37afd-189">**Nivel de protección de los ACP de COPP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="37afd-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="37afd-190">CGMS-A</span></span>               | [<span data-ttu-id="37afd-191">**Nivel de protección de COPP \_ CGMSA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="37afd-192">HDCP</span><span class="sxs-lookup"><span data-stu-id="37afd-192">HDCP</span></span>                 | [<span data-ttu-id="37afd-193">**\_Nivel de \_ protección de HDCP de COPP \_**</span><span class="sxs-lookup"><span data-stu-id="37afd-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="37afd-194">Consulta de tipo de protección</span><span class="sxs-lookup"><span data-stu-id="37afd-194">Protection Type Query</span></span>

<span data-ttu-id="37afd-195">Devuelve los mecanismos de protección que están disponibles para el conector.</span><span class="sxs-lookup"><span data-stu-id="37afd-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="37afd-196">**GUID**: DXVA \_ COPPQueryProtectionType</span><span class="sxs-lookup"><span data-stu-id="37afd-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="37afd-197">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-197">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-198">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="37afd-199">Los mecanismos de protección se devuelven en el miembro **dwData** como una combinación de cero o más marcadores.</span><span class="sxs-lookup"><span data-stu-id="37afd-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="37afd-200">Consulte [marcas de tipo de protección COPP](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="37afd-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="37afd-201">Si hay más de un mecanismo de protección disponible, las marcas se combinan con una **operación OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="37afd-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="37afd-202">Consulta de señalización</span><span class="sxs-lookup"><span data-stu-id="37afd-202">Signaling Query</span></span>

<span data-ttu-id="37afd-203">Devuelve una lista de todos los estándares de protección admitidos por el controlador, el estándar que está activo actualmente y la relación de aspecto actual u otros datos de señalización.</span><span class="sxs-lookup"><span data-stu-id="37afd-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="37afd-204">**GUID**: DXVA \_ COPPQuerySignaling</span><span class="sxs-lookup"><span data-stu-id="37afd-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="37afd-205">**Datos de entrada**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="37afd-205">**Input data**: None.</span></span>
-   <span data-ttu-id="37afd-206">**Devolver datos**: devuelve una estructura de [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="37afd-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37afd-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37afd-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37afd-208">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="37afd-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



