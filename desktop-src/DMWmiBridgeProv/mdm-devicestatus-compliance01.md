---
title: MDM_DeviceStatus_Compliance01 (clase)
description: La \_ \_ clase Compliance01 de DEVICESTATUS de MDM permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- MDM_DeviceStatus_Compliance01 (clase)
- MDM_DeviceStatus_Compliance01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150728"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="534c3-105">\_Clase Compliance01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="534c3-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="534c3-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="534c3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="534c3-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="534c3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="534c3-108">La **clase \_ \_ Compliance01 de DeviceStatus de MDM** permite consultar si el dispositivo cumple con la Directiva de cifrado empresarial.</span><span class="sxs-lookup"><span data-stu-id="534c3-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="534c3-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="534c3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="534c3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="534c3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="534c3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="534c3-111">Members</span></span>

<span data-ttu-id="534c3-112">La **clase \_ \_ Compliance01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="534c3-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="534c3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="534c3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="534c3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="534c3-114">Properties</span></span>

<span data-ttu-id="534c3-115">La **clase \_ \_ Compliance01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="534c3-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="534c3-116">EncryptionCompliance</span><span class="sxs-lookup"><span data-stu-id="534c3-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534c3-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="534c3-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="534c3-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="534c3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="534c3-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="534c3-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="534c3-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="534c3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534c3-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="534c3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="534c3-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="534c3-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="534c3-123">Nodo para consultas en cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="534c3-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="534c3-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="534c3-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="534c3-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="534c3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534c3-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="534c3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="534c3-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="534c3-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="534c3-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="534c3-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="534c3-129">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="534c3-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="534c3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="534c3-130">Requirements</span></span>



| <span data-ttu-id="534c3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="534c3-131">Requirement</span></span> | <span data-ttu-id="534c3-132">Value</span><span class="sxs-lookup"><span data-stu-id="534c3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="534c3-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="534c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="534c3-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="534c3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="534c3-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="534c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="534c3-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="534c3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="534c3-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="534c3-137">Namespace</span></span><br/>                | <span data-ttu-id="534c3-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="534c3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="534c3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="534c3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="534c3-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="534c3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="534c3-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="534c3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="534c3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="534c3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534c3-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="534c3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534c3-144">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="534c3-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

