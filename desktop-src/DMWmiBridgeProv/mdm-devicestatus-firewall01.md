---
title: MDM_DeviceStatus_Firewall01 (clase)
description: '\_ \_ La empresa usa la clase Firewall01 de DEVICESTATUS de MDM para consultar el estado de compatibilidad del firewall de los dispositivos con sus directivas de empresa.'
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- MDM_DeviceStatus_Firewall01 (clase)
- MDM_DeviceStatus_Firewall01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803121"
---
# <a name="mdm_devicestatus_firewall01-class"></a><span data-ttu-id="d85ca-105">\_Clase Firewall01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="d85ca-105">MDM\_DeviceStatus\_Firewall01 class</span></span>

<span data-ttu-id="d85ca-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d85ca-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d85ca-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d85ca-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d85ca-108">La empresa usa la clase **\_ \_ Firewall01 de DeviceStatus de MDM** para consultar el estado de compatibilidad del firewall de los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="d85ca-108">The **MDM\_DeviceStatus\_Firewall01** class is used by the enterprise to query the state of firewall compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="d85ca-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d85ca-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85ca-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d85ca-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="d85ca-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d85ca-111">Members</span></span>

<span data-ttu-id="d85ca-112">La **clase \_ \_ Firewall01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d85ca-112">The **MDM\_DeviceStatus\_Firewall01** class has these types of members:</span></span>

-   [<span data-ttu-id="d85ca-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d85ca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d85ca-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d85ca-114">Properties</span></span>

<span data-ttu-id="d85ca-115">La **clase \_ \_ Firewall01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d85ca-115">The **MDM\_DeviceStatus\_Firewall01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d85ca-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d85ca-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d85ca-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d85ca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d85ca-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d85ca-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d85ca-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d85ca-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d85ca-120">Nodo para la consulta de Firewall.</span><span class="sxs-lookup"><span data-stu-id="d85ca-120">Node for the firewall query.</span></span>

</dd> <dt>

<span data-ttu-id="d85ca-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d85ca-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d85ca-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d85ca-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d85ca-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d85ca-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d85ca-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d85ca-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d85ca-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d85ca-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d85ca-126">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="d85ca-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="d85ca-127">Estado</span><span class="sxs-lookup"><span data-stu-id="d85ca-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d85ca-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d85ca-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d85ca-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d85ca-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d85ca-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d85ca-130">Requirements</span></span>



| <span data-ttu-id="d85ca-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d85ca-131">Requirement</span></span> | <span data-ttu-id="d85ca-132">Value</span><span class="sxs-lookup"><span data-stu-id="d85ca-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d85ca-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85ca-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d85ca-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d85ca-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d85ca-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85ca-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d85ca-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d85ca-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d85ca-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d85ca-137">Namespace</span></span><br/>                | <span data-ttu-id="d85ca-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d85ca-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d85ca-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d85ca-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d85ca-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d85ca-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d85ca-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d85ca-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d85ca-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d85ca-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

