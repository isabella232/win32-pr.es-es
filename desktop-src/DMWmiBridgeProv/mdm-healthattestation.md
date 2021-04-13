---
title: MDM_HealthAttestation (clase)
description: La \_ clase HealthAttestation de MDM permite a los administradores de TI empresariales evaluar el estado de los dispositivos administrados y realizar acciones de directiva de empresa.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation (clase)
- MDM_HealthAttestation clase, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489934"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="1c238-105">\_Clase HealthAttestation de MDM</span><span class="sxs-lookup"><span data-stu-id="1c238-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="1c238-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1c238-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1c238-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1c238-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c238-108">La **clase \_ HealthAttestation de MDM** permite a los administradores de TI empresariales evaluar el estado de los dispositivos administrados y realizar acciones de directiva de empresa.</span><span class="sxs-lookup"><span data-stu-id="1c238-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="1c238-109">A continuación se muestra una lista de las funciones realizadas por el CSP HealthAttestation:</span><span class="sxs-lookup"><span data-stu-id="1c238-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="1c238-110">Recopila datos que se usan en la comprobación de los Estados de mantenimiento de los dispositivos</span><span class="sxs-lookup"><span data-stu-id="1c238-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="1c238-111">Reenvía los datos al servicio de atestación de estado (HAS)</span><span class="sxs-lookup"><span data-stu-id="1c238-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="1c238-112">Aprovisiona que el certificado de atestación de estado que recibe de tiene</span><span class="sxs-lookup"><span data-stu-id="1c238-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="1c238-113">Tras la solicitud, reenvía el certificado de atestación de estado (recibido de tiene) y la información relacionada en tiempo de ejecución al servidor MDM para su comprobación</span><span class="sxs-lookup"><span data-stu-id="1c238-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="1c238-114">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1c238-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c238-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c238-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="1c238-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c238-116">Members</span></span>

<span data-ttu-id="1c238-117">La **clase \_ HealthAttestation de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1c238-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="1c238-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c238-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c238-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c238-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c238-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c238-120">Methods</span></span>

<span data-ttu-id="1c238-121">La **clase \_ HealthAttestation de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1c238-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="1c238-122">Método</span><span class="sxs-lookup"><span data-stu-id="1c238-122">Method</span></span>                                                                 | <span data-ttu-id="1c238-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c238-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c238-124">**VerifyHealthMethod**</span><span class="sxs-lookup"><span data-stu-id="1c238-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="1c238-125">Método para notificar al dispositivo que prepare una solicitud de comprobación de certificado de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="1c238-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1c238-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c238-126">Properties</span></span>

<span data-ttu-id="1c238-127">La **clase \_ HealthAttestation de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c238-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1c238-128">Certificate</span><span class="sxs-lookup"><span data-stu-id="1c238-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1c238-131">Calificadores: **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="1c238-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c238-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="1c238-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c238-135">**CurrentProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="1c238-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-136">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c238-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1c238-138">TBD</span><span class="sxs-lookup"><span data-stu-id="1c238-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="1c238-139">ForceRetrieve</span><span class="sxs-lookup"><span data-stu-id="1c238-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1c238-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c238-142">HASEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c238-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c238-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c238-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c238-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c238-148">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c238-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c238-149">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1c238-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="1c238-150">Para esta clase, la cadena es "HealthAttestation".</span><span class="sxs-lookup"><span data-stu-id="1c238-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="1c238-151">**MaxSupportedProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="1c238-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-152">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c238-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1c238-154">TBD</span><span class="sxs-lookup"><span data-stu-id="1c238-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="1c238-155">Emisor</span><span class="sxs-lookup"><span data-stu-id="1c238-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c238-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1c238-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1c238-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c238-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c238-161">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c238-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c238-162">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1c238-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="1c238-163">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="1c238-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="1c238-164">**PreferredMaxProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="1c238-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c238-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1c238-167">TBD</span><span class="sxs-lookup"><span data-stu-id="1c238-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="1c238-168">Estado</span><span class="sxs-lookup"><span data-stu-id="1c238-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-169">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c238-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c238-171">TpmReadyStatus</span><span class="sxs-lookup"><span data-stu-id="1c238-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c238-172">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c238-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c238-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1c238-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c238-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c238-174">Requirements</span></span>



| <span data-ttu-id="1c238-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c238-175">Requirement</span></span> | <span data-ttu-id="1c238-176">Value</span><span class="sxs-lookup"><span data-stu-id="1c238-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c238-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c238-177">Minimum supported client</span></span><br/> | <span data-ttu-id="1c238-178">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c238-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c238-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c238-179">Minimum supported server</span></span><br/> | <span data-ttu-id="1c238-180">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1c238-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1c238-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c238-181">Namespace</span></span><br/>                | <span data-ttu-id="1c238-182">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1c238-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1c238-183">MOF</span><span class="sxs-lookup"><span data-stu-id="1c238-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c238-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c238-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c238-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c238-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c238-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c238-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c238-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c238-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c238-188">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="1c238-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

