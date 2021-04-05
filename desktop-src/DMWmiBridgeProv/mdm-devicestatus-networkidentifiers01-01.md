---
title: MDM_DeviceStatus_NetworkIdentifiers01_01 (clase)
description: La \_ clase DeviceStatus \_ NetworkIdentifiers01 \_ 01 de MDM permite consultar las propiedades de red de un dispositivo.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- MDM_DeviceStatus_NetworkIdentifiers01_01 (clase)
- MDM_DeviceStatus_NetworkIdentifiers01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530c301894d957c9a9a2db374f35cf7c1bcb5063
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079599"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a><span data-ttu-id="49f9d-105">\_Clase DeviceStatus \_ NetworkIdentifiers01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="49f9d-105">MDM\_DeviceStatus\_NetworkIdentifiers01\_01 class</span></span>

<span data-ttu-id="49f9d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="49f9d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="49f9d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="49f9d-108">La **clase \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01 de MDM** permite consultar las propiedades de red de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49f9d-108">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class allows you to query a device for network properties.</span></span>

<span data-ttu-id="49f9d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="49f9d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f9d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49f9d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a><span data-ttu-id="49f9d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="49f9d-111">Members</span></span>

<span data-ttu-id="49f9d-112">La **clase \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="49f9d-112">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="49f9d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49f9d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49f9d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49f9d-114">Properties</span></span>

<span data-ttu-id="49f9d-115">La **clase \_ DeviceStatus \_ NetworkIdentifiers01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="49f9d-115">The **MDM\_DeviceStatus\_NetworkIdentifiers01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49f9d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="49f9d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49f9d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49f9d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49f9d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="49f9d-120">Nodo para las consultas en las propiedades de red y dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49f9d-120">Node for queries on network and device properties.</span></span>

</dd> <dt>

[<span data-ttu-id="49f9d-121">IPAddressV4</span><span class="sxs-lookup"><span data-stu-id="49f9d-121">IPAddressV4</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49f9d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49f9d-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49f9d-124">IPAddressV6</span><span class="sxs-lookup"><span data-stu-id="49f9d-124">IPAddressV6</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49f9d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49f9d-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49f9d-127">IsConnected</span><span class="sxs-lookup"><span data-stu-id="49f9d-127">IsConnected</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="49f9d-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49f9d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="49f9d-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="49f9d-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49f9d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49f9d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49f9d-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="49f9d-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="49f9d-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="49f9d-135">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="49f9d-135">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="49f9d-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="49f9d-136">Type</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f9d-137">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="49f9d-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f9d-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49f9d-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49f9d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49f9d-139">Requirements</span></span>



| <span data-ttu-id="49f9d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f9d-140">Requirement</span></span> | <span data-ttu-id="49f9d-141">Value</span><span class="sxs-lookup"><span data-stu-id="49f9d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f9d-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49f9d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="49f9d-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49f9d-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49f9d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="49f9d-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49f9d-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="49f9d-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49f9d-146">Namespace</span></span><br/>                | <span data-ttu-id="49f9d-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="49f9d-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="49f9d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="49f9d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49f9d-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49f9d-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="49f9d-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49f9d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49f9d-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f9d-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f9d-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="49f9d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f9d-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="49f9d-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

