---
title: MDM_DevDetail_Microsoft02 (clase)
description: La \_ clase Microsoft02 de DevDetail de MDM \_ controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- MDM_DevDetail_Microsoft02 (clase)
- MDM_DevDetail_Microsoft02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996794"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="6089c-105">\_Clase Microsoft02 DevDetail de MDM \_</span><span class="sxs-lookup"><span data-stu-id="6089c-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="6089c-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6089c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6089c-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6089c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6089c-108">La **clase \_ \_ Microsoft02 de DevDetail de MDM** controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="6089c-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="6089c-109">Estos parámetros de dispositivo no se envían automáticamente desde el cliente al servidor, sino que se pueden consultar mediante los comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="6089c-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="6089c-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6089c-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6089c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6089c-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="6089c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="6089c-112">Members</span></span>

<span data-ttu-id="6089c-113">La **clase \_ \_ Microsoft02 de MDM DevDetail** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6089c-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="6089c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6089c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6089c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6089c-115">Properties</span></span>

<span data-ttu-id="6089c-116">La **clase \_ \_ Microsoft02 de MDM DevDetail** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6089c-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6089c-117">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="6089c-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6089c-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="6089c-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6089c-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6089c-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6089c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6089c-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6089c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6089c-127">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6089c-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="6089c-128">Para esta clase, la cadena es "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="6089c-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="6089c-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="6089c-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6089c-132">MobileID</span><span class="sxs-lookup"><span data-stu-id="6089c-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6089c-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="6089c-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6089c-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6089c-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6089c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6089c-141">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6089c-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6089c-142">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6089c-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="6089c-143">Para esta clase, la cadena es "./DevDetail/Ext".</span><span class="sxs-lookup"><span data-stu-id="6089c-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="6089c-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6089c-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-145">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6089c-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6089c-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="6089c-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-148">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6089c-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6089c-150">RadioSwV</span><span class="sxs-lookup"><span data-stu-id="6089c-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6089c-153">Devuelve el número de versión del software de pila de radio.</span><span class="sxs-lookup"><span data-stu-id="6089c-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="6089c-154">Resolución</span><span class="sxs-lookup"><span data-stu-id="6089c-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6089c-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6089c-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6089c-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6089c-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6089c-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6089c-157">Requirements</span></span>



| <span data-ttu-id="6089c-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6089c-158">Requirement</span></span> | <span data-ttu-id="6089c-159">Value</span><span class="sxs-lookup"><span data-stu-id="6089c-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6089c-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6089c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6089c-161">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6089c-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6089c-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6089c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6089c-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6089c-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6089c-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6089c-164">Namespace</span></span><br/>                | <span data-ttu-id="6089c-165">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="6089c-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6089c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6089c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6089c-167"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6089c-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6089c-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6089c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6089c-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6089c-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6089c-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="6089c-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6089c-171">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="6089c-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

