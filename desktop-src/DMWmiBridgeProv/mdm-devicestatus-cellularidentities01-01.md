---
title: MDM_DeviceStatus_CellularIdentities01_01 (clase)
description: La \_ clase DeviceStatus \_ CellularIdentities01 \_ 01 de MDM le permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- MDM_DeviceStatus_CellularIdentities01_01 (clase)
- MDM_DeviceStatus_CellularIdentities01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d9d3fab514fbfb56d132fc20ba98ef8c2565eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905440"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a><span data-ttu-id="01e3f-105">\_Clase DeviceStatus \_ CellularIdentities01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="01e3f-105">MDM\_DeviceStatus\_CellularIdentities01\_01 class</span></span>

<span data-ttu-id="01e3f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="01e3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01e3f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="01e3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01e3f-108">La **clase \_ DeviceStatus \_ CellularIdentities01 \_ 01 de MDM** le permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.</span><span class="sxs-lookup"><span data-stu-id="01e3f-108">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="01e3f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01e3f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e3f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01e3f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a><span data-ttu-id="01e3f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="01e3f-111">Members</span></span>

<span data-ttu-id="01e3f-112">La **clase \_ DeviceStatus \_ CellularIdentities01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01e3f-112">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="01e3f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01e3f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01e3f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01e3f-114">Properties</span></span>

<span data-ttu-id="01e3f-115">La **clase \_ DeviceStatus \_ CellularIdentities01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01e3f-115">The **MDM\_DeviceStatus\_CellularIdentities01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="01e3f-116">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="01e3f-116">CommercializationOperator</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e3f-119">ICCID</span><span class="sxs-lookup"><span data-stu-id="01e3f-119">ICCID</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e3f-122">IMSI</span><span class="sxs-lookup"><span data-stu-id="01e3f-122">IMSI</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01e3f-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01e3f-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01e3f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01e3f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01e3f-129">Nodo para las consultas en tarjetas SIM.</span><span class="sxs-lookup"><span data-stu-id="01e3f-129">Node for queries on SIM cards.</span></span>

</dd> <dt>

<span data-ttu-id="01e3f-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="01e3f-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01e3f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01e3f-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01e3f-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="01e3f-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="01e3f-135">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="01e3f-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="01e3f-136">Teléfono</span><span class="sxs-lookup"><span data-stu-id="01e3f-136">PhoneNumber</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01e3f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e3f-139">RoamingCompliance</span><span class="sxs-lookup"><span data-stu-id="01e3f-139">RoamingCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="01e3f-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e3f-142">RoamingStatus</span><span class="sxs-lookup"><span data-stu-id="01e3f-142">RoamingStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e3f-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="01e3f-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e3f-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01e3f-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01e3f-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e3f-145">Requirements</span></span>



| <span data-ttu-id="01e3f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e3f-146">Requirement</span></span> | <span data-ttu-id="01e3f-147">Value</span><span class="sxs-lookup"><span data-stu-id="01e3f-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e3f-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01e3f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="01e3f-149">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="01e3f-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01e3f-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01e3f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="01e3f-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="01e3f-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="01e3f-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01e3f-152">Namespace</span></span><br/>                | <span data-ttu-id="01e3f-153">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="01e3f-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="01e3f-154">MOF</span><span class="sxs-lookup"><span data-stu-id="01e3f-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01e3f-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01e3f-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="01e3f-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01e3f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e3f-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e3f-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e3f-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="01e3f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e3f-159">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="01e3f-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

