---
title: MDM_DeviceStatus_Antispyware01 (clase)
description: '\_ \_ La empresa usa la clase Antispyware01 de DEVICESTATUS de MDM para consultar el estado de cumplimiento de anti spyware de los dispositivos con sus directivas de empresa.'
ms.assetid: 53275aa1-ff7d-4630-b6c5-aedce3f4665a
keywords:
- MDM_DeviceStatus_Antispyware01 (clase)
- MDM_DeviceStatus_Antispyware01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01.InstanceID
- MDM_DeviceStatus_Antispyware01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91468c98981c93e211b3e3bee99564574f7a56cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905441"
---
# <a name="mdm_devicestatus_antispyware01-class"></a><span data-ttu-id="1e946-105">\_Clase Antispyware01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="1e946-105">MDM\_DeviceStatus\_Antispyware01 class</span></span>

<span data-ttu-id="1e946-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1e946-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e946-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1e946-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e946-108">La empresa usa la clase **\_ \_ Antispyware01 de DeviceStatus de MDM** para consultar el estado de cumplimiento de anti spyware de los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="1e946-108">The **MDM\_DeviceStatus\_Antispyware01** class is used by the enterprise to query the state of antispyware compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="1e946-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e946-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e946-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e946-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antispyware01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="1e946-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e946-111">Members</span></span>

<span data-ttu-id="1e946-112">La **clase \_ \_ Antispyware01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e946-112">The **MDM\_DeviceStatus\_Antispyware01** class has these types of members:</span></span>

-   [<span data-ttu-id="1e946-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e946-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e946-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e946-114">Properties</span></span>

<span data-ttu-id="1e946-115">La **clase \_ \_ Antispyware01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e946-115">The **MDM\_DeviceStatus\_Antispyware01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e946-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e946-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e946-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e946-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e946-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e946-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e946-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e946-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e946-120">Nodo para la consulta de anti spyware.</span><span class="sxs-lookup"><span data-stu-id="1e946-120">Node for the antispyware query.</span></span>

</dd> <dt>

<span data-ttu-id="1e946-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1e946-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e946-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e946-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e946-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e946-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e946-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e946-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e946-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1e946-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="1e946-126">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="1e946-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="1e946-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="1e946-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e946-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1e946-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e946-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e946-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e946-130">Estado</span><span class="sxs-lookup"><span data-stu-id="1e946-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e946-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1e946-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e946-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e946-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e946-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e946-133">Requirements</span></span>



| <span data-ttu-id="1e946-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e946-134">Requirement</span></span> | <span data-ttu-id="1e946-135">Value</span><span class="sxs-lookup"><span data-stu-id="1e946-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e946-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e946-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e946-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e946-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e946-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e946-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e946-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e946-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e946-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e946-140">Namespace</span></span><br/>                | <span data-ttu-id="1e946-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1e946-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e946-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1e946-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e946-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e946-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e946-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e946-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e946-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e946-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

