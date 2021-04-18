---
title: MDM_RemoteFind_Location01 (clase)
description: La \_ \_ clase Location01 de REMOTEFIND de MDM recupera la información de ubicación de un dispositivo determinado.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01 (clase)
- MDM_RemoteFind_Location01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489179"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="b5a87-105">\_Clase Location01 RemoteFind de MDM \_</span><span class="sxs-lookup"><span data-stu-id="b5a87-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="b5a87-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b5a87-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b5a87-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b5a87-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b5a87-108">La **clase \_ \_ Location01 de RemoteFind de MDM** recupera la información de ubicación de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="b5a87-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="b5a87-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b5a87-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a87-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5a87-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="b5a87-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5a87-111">Members</span></span>

<span data-ttu-id="b5a87-112">La **clase \_ \_ Location01 de MDM RemoteFind** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b5a87-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="b5a87-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5a87-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5a87-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5a87-114">Properties</span></span>

<span data-ttu-id="b5a87-115">La **clase \_ \_ Location01 de MDM RemoteFind** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b5a87-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b5a87-116">Precisión</span><span class="sxs-lookup"><span data-stu-id="b5a87-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b5a87-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5a87-119">Age</span><span class="sxs-lookup"><span data-stu-id="b5a87-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-120">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5a87-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5a87-122">Altitud</span><span class="sxs-lookup"><span data-stu-id="b5a87-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-123">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5a87-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5a87-125">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="b5a87-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b5a87-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5a87-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5a87-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b5a87-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5a87-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5a87-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b5a87-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b5a87-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="b5a87-133">Para esta clase, la cadena es "Location".</span><span class="sxs-lookup"><span data-stu-id="b5a87-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="b5a87-134">Latitud</span><span class="sxs-lookup"><span data-stu-id="b5a87-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-135">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5a87-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5a87-137">Longitud</span><span class="sxs-lookup"><span data-stu-id="b5a87-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-138">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5a87-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b5a87-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5a87-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b5a87-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5a87-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b5a87-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5a87-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5a87-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5a87-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b5a87-144">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b5a87-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="b5a87-145">Para esta clase, la cadena es "./Vendor/MSFT/RemoteFind".</span><span class="sxs-lookup"><span data-stu-id="b5a87-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5a87-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a87-146">Requirements</span></span>



| <span data-ttu-id="b5a87-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a87-147">Requirement</span></span> | <span data-ttu-id="b5a87-148">Value</span><span class="sxs-lookup"><span data-stu-id="b5a87-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a87-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a87-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a87-150">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5a87-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5a87-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a87-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a87-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b5a87-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b5a87-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5a87-153">Namespace</span></span><br/>                | <span data-ttu-id="b5a87-154">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b5a87-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b5a87-155">MOF</span><span class="sxs-lookup"><span data-stu-id="b5a87-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5a87-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5a87-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5a87-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5a87-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a87-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5a87-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5a87-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5a87-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a87-160">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="b5a87-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

