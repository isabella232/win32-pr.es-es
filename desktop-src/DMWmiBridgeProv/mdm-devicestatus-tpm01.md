---
title: MDM_DeviceStatus_TPM01 (clase)
description: '\_ \_ La empresa usa la clase TPM01 de DEVICESTATUS de MDM para consultar la versión de TPM de los dispositivos con sus directivas de empresa.'
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- MDM_DeviceStatus_TPM01 (clase)
- MDM_DeviceStatus_TPM01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905438"
---
# <a name="mdm_devicestatus_tpm01-class"></a><span data-ttu-id="f18d1-105">\_Clase TPM01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="f18d1-105">MDM\_DeviceStatus\_TPM01 class</span></span>

<span data-ttu-id="f18d1-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f18d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f18d1-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f18d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f18d1-108">La empresa usa la clase **\_ \_ TPM01 de DeviceStatus de MDM** para consultar la versión de TPM de los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="f18d1-108">The **MDM\_DeviceStatus\_TPM01** class is used by the enterprise to query the TPM version of devices with their enterprise policies.</span></span>

<span data-ttu-id="f18d1-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f18d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18d1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f18d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a><span data-ttu-id="f18d1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f18d1-111">Members</span></span>

<span data-ttu-id="f18d1-112">La **clase \_ \_ TPM01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f18d1-112">The **MDM\_DeviceStatus\_TPM01** class has these types of members:</span></span>

-   [<span data-ttu-id="f18d1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f18d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f18d1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f18d1-114">Properties</span></span>

<span data-ttu-id="f18d1-115">La **clase \_ \_ TPM01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f18d1-115">The **MDM\_DeviceStatus\_TPM01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f18d1-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f18d1-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f18d1-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f18d1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f18d1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f18d1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f18d1-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f18d1-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f18d1-120">Nodo para la consulta de TPM.</span><span class="sxs-lookup"><span data-stu-id="f18d1-120">Node for the TPM query.</span></span>

</dd> <dt>

<span data-ttu-id="f18d1-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f18d1-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f18d1-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f18d1-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f18d1-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f18d1-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f18d1-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f18d1-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f18d1-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f18d1-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="f18d1-126">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="f18d1-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="f18d1-127">SpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="f18d1-127">SpecificationVersion</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f18d1-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f18d1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f18d1-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f18d1-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f18d1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f18d1-130">Requirements</span></span>



| <span data-ttu-id="f18d1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f18d1-131">Requirement</span></span> | <span data-ttu-id="f18d1-132">Value</span><span class="sxs-lookup"><span data-stu-id="f18d1-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18d1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f18d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f18d1-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f18d1-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f18d1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f18d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f18d1-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f18d1-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f18d1-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f18d1-137">Namespace</span></span><br/>                | <span data-ttu-id="f18d1-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f18d1-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f18d1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f18d1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f18d1-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f18d1-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f18d1-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f18d1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f18d1-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f18d1-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

