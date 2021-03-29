---
title: MDM_DeviceStatus_Antivirus01 (clase)
description: '\_ \_ La empresa usa la clase Antivirus01 de DEVICESTATUS de MDM para consultar el estado de cumplimiento antivirus de dispositivos con sus directivas empresariales.'
ms.assetid: 8b3145a6-b836-4750-a0c3-88472f9a12c5
keywords:
- MDM_DeviceStatus_Antivirus01 (clase)
- MDM_DeviceStatus_Antivirus01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antivirus01
- MDM_DeviceStatus_Antivirus01.InstanceID
- MDM_DeviceStatus_Antivirus01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3197dddb9bea498de63d08a025050963d4348054
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491969"
---
# <a name="mdm_devicestatus_antivirus01-class"></a><span data-ttu-id="01a1a-105">\_Clase Antivirus01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="01a1a-105">MDM\_DeviceStatus\_Antivirus01 class</span></span>

<span data-ttu-id="01a1a-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="01a1a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01a1a-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="01a1a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01a1a-108">La empresa usa la clase **\_ \_ Antivirus01 de DeviceStatus de MDM** para consultar el estado de cumplimiento antivirus de dispositivos con sus directivas empresariales.</span><span class="sxs-lookup"><span data-stu-id="01a1a-108">The **MDM\_DeviceStatus\_Antivirus01** class is used by the enterprise to query the state of antivirus compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="01a1a-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01a1a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a1a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01a1a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antivirus01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="01a1a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="01a1a-111">Members</span></span>

<span data-ttu-id="01a1a-112">La **clase \_ \_ Antivirus01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01a1a-112">The **MDM\_DeviceStatus\_Antivirus01** class has these types of members:</span></span>

-   [<span data-ttu-id="01a1a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01a1a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01a1a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01a1a-114">Properties</span></span>

<span data-ttu-id="01a1a-115">La **clase \_ \_ Antivirus01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01a1a-115">The **MDM\_DeviceStatus\_Antivirus01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01a1a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01a1a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1a-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01a1a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01a1a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a1a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a1a-120">Nodo para la consulta antivirus.</span><span class="sxs-lookup"><span data-stu-id="01a1a-120">Node for the antivirus query.</span></span>

</dd> <dt>

<span data-ttu-id="01a1a-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="01a1a-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1a-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01a1a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01a1a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a1a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a1a-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="01a1a-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="01a1a-126">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="01a1a-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="01a1a-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="01a1a-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1a-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a1a-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01a1a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01a1a-130">Estado</span><span class="sxs-lookup"><span data-stu-id="01a1a-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a1a-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="01a1a-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01a1a-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01a1a-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01a1a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a1a-133">Requirements</span></span>



| <span data-ttu-id="01a1a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a1a-134">Requirement</span></span> | <span data-ttu-id="01a1a-135">Value</span><span class="sxs-lookup"><span data-stu-id="01a1a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a1a-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a1a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="01a1a-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="01a1a-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01a1a-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a1a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="01a1a-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="01a1a-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="01a1a-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01a1a-140">Namespace</span></span><br/>                | <span data-ttu-id="01a1a-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="01a1a-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="01a1a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="01a1a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01a1a-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01a1a-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="01a1a-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01a1a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a1a-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a1a-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

