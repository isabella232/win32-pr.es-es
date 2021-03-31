---
title: MDM_RemoteFind (clase)
description: La \_ clase RemoteFind de MDM recupera la información de ubicación de un dispositivo determinado.
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- MDM_RemoteFind (clase)
- MDM_RemoteFind clase, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801207"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="ed5ec-105">\_Clase RemoteFind de MDM</span><span class="sxs-lookup"><span data-stu-id="ed5ec-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="ed5ec-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed5ec-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ed5ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed5ec-108">La **clase \_ RemoteFind de MDM** recupera la información de ubicación de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="ed5ec-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5ec-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed5ec-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="ed5ec-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed5ec-111">Members</span></span>

<span data-ttu-id="ed5ec-112">La **clase \_ RemoteFind de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ed5ec-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="ed5ec-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed5ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed5ec-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed5ec-114">Properties</span></span>

<span data-ttu-id="ed5ec-115">La **clase \_ RemoteFind de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ed5ec-116">DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="ed5ec-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5ec-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ed5ec-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed5ec-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5ec-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed5ec-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed5ec-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed5ec-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ed5ec-124">Para esta clase, la cadena es "RemoteFind".</span><span class="sxs-lookup"><span data-stu-id="ed5ec-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="ed5ec-125">Máximo</span><span class="sxs-lookup"><span data-stu-id="ed5ec-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5ec-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ed5ec-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed5ec-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5ec-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed5ec-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed5ec-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed5ec-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="ed5ec-133">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="ed5ec-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="ed5ec-134">Tiempo de espera</span><span class="sxs-lookup"><span data-stu-id="ed5ec-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed5ec-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed5ec-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed5ec-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ed5ec-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed5ec-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed5ec-137">Requirements</span></span>



| <span data-ttu-id="ed5ec-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed5ec-138">Requirement</span></span> | <span data-ttu-id="ed5ec-139">Value</span><span class="sxs-lookup"><span data-stu-id="ed5ec-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5ec-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed5ec-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5ec-141">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed5ec-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed5ec-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed5ec-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5ec-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ed5ec-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ed5ec-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed5ec-144">Namespace</span></span><br/>                | <span data-ttu-id="ed5ec-145">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ed5ec-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="ed5ec-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ed5ec-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed5ec-147"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed5ec-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed5ec-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed5ec-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed5ec-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed5ec-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ed5ec-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed5ec-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5ec-151">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="ed5ec-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

