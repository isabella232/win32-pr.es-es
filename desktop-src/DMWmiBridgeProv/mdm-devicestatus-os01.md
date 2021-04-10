---
title: MDM_DeviceStatus_OS01 (clase)
description: '\_ \_ La empresa usa la clase OS01 de DEVICESTATUS de MDM para consultar el sistema operativo en los dispositivos con sus directivas de empresa.'
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- MDM_DeviceStatus_OS01 (clase)
- MDM_DeviceStatus_OS01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150726"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="5c837-105">\_Clase OS01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="5c837-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="5c837-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5c837-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5c837-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5c837-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5c837-108">La empresa usa la clase **\_ \_ OS01 de DeviceStatus de MDM** para consultar el sistema operativo en los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="5c837-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="5c837-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5c837-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c837-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c837-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="5c837-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c837-111">Members</span></span>

<span data-ttu-id="5c837-112">La **clase \_ \_ OS01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c837-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="5c837-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c837-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c837-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c837-114">Properties</span></span>

<span data-ttu-id="5c837-115">La **clase \_ \_ OS01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c837-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5c837-116">Edición</span><span class="sxs-lookup"><span data-stu-id="5c837-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c837-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c837-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c837-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5c837-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c837-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c837-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c837-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c837-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c837-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c837-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c837-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c837-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5c837-123">Nodo para la consulta de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5c837-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="5c837-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5c837-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c837-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c837-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c837-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c837-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c837-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c837-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5c837-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5c837-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="5c837-129">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="5c837-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c837-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c837-130">Requirements</span></span>



| <span data-ttu-id="5c837-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c837-131">Requirement</span></span> | <span data-ttu-id="5c837-132">Value</span><span class="sxs-lookup"><span data-stu-id="5c837-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c837-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c837-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c837-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c837-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c837-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c837-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c837-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5c837-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5c837-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c837-137">Namespace</span></span><br/>                | <span data-ttu-id="5c837-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="5c837-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5c837-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5c837-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c837-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c837-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c837-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c837-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c837-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c837-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

