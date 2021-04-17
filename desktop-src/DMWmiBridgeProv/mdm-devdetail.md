---
title: MDM_DevDetail (clase)
description: La \_ clase DevDetail de MDM controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- MDM_DevDetail (clase)
- MDM_DevDetail clase, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658283"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="0b1f9-105">\_Clase DevDetail de MDM</span><span class="sxs-lookup"><span data-stu-id="0b1f9-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="0b1f9-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b1f9-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0b1f9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b1f9-108">La **clase \_ DevDetail de MDM** controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="0b1f9-109">Estos parámetros de dispositivo no se envían automáticamente desde el cliente al servidor, sino que se pueden consultar mediante los comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="0b1f9-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1f9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b1f9-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="0b1f9-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b1f9-112">Members</span></span>

<span data-ttu-id="0b1f9-113">La **clase \_ DevDetail de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b1f9-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="0b1f9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b1f9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b1f9-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b1f9-115">Properties</span></span>

<span data-ttu-id="0b1f9-116">La **clase \_ DevDetail de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b1f9-117">DevTyp</span><span class="sxs-lookup"><span data-stu-id="0b1f9-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b1f9-120">FwV</span><span class="sxs-lookup"><span data-stu-id="0b1f9-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b1f9-123">HwV</span><span class="sxs-lookup"><span data-stu-id="0b1f9-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b1f9-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b1f9-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b1f9-130">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="0b1f9-131">Para esta clase, la cadena es "DevDetail".</span><span class="sxs-lookup"><span data-stu-id="0b1f9-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="0b1f9-132">LrgObj</span><span class="sxs-lookup"><span data-stu-id="0b1f9-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b1f9-135">OEM</span><span class="sxs-lookup"><span data-stu-id="0b1f9-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b1f9-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-141">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b1f9-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b1f9-142">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b1f9-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="0b1f9-143">SwV</span><span class="sxs-lookup"><span data-stu-id="0b1f9-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b1f9-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b1f9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b1f9-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b1f9-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b1f9-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b1f9-146">Requirements</span></span>



| <span data-ttu-id="0b1f9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b1f9-147">Requirement</span></span> | <span data-ttu-id="0b1f9-148">Value</span><span class="sxs-lookup"><span data-stu-id="0b1f9-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1f9-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b1f9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1f9-150">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b1f9-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b1f9-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b1f9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1f9-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b1f9-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b1f9-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b1f9-153">Namespace</span></span><br/>                | <span data-ttu-id="0b1f9-154">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0b1f9-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b1f9-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0b1f9-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b1f9-156"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b1f9-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b1f9-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b1f9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b1f9-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b1f9-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b1f9-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b1f9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1f9-160">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="0b1f9-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

