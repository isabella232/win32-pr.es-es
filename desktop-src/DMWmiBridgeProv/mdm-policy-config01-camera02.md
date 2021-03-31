---
title: MDM_Policy_Config01_Camera02 (clase)
description: La \_ clase MDM Policy \_ Config01 \_ Camera02 representa las directivas de cámara disponibles.
ms.assetid: dd17c2bc-8c96-4f5e-a4d2-cf1d27a92eb7
keywords:
- MDM_Policy_Config01_Camera02 (clase)
- MDM_Policy_Config01_Camera02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Camera02
- MDM_Policy_Config01_Camera02.InstanceID
- MDM_Policy_Config01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 377a9eb695560d7bf93fd6a5d761b1e95202bf20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801879"
---
# <a name="mdm_policy_config01_camera02-class"></a><span data-ttu-id="8f7f4-105">\_ \_ Clase Camera02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="8f7f4-105">MDM\_Policy\_Config01\_Camera02 class</span></span>

<span data-ttu-id="8f7f4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8f7f4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="8f7f4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8f7f4-108">La clase **MDM \_ Policy \_ Config01 \_ Camera02** representa las directivas de cámara disponibles.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-108">The **MDM\_Policy\_Config01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="8f7f4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7f4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f7f4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="8f7f4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f7f4-111">Members</span></span>

<span data-ttu-id="8f7f4-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Camera02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8f7f4-112">The **MDM\_Policy\_Config01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="8f7f4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f7f4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f7f4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f7f4-114">Properties</span></span>

<span data-ttu-id="8f7f4-115">La **clase \_ \_ Config01 de \_ Camera02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-115">The **MDM\_Policy\_Config01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8f7f4-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="8f7f4-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f7f4-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f7f4-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8f7f4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f7f4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f7f4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f7f4-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f7f4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f7f4-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f7f4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f7f4-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8f7f4-124">Para esta clase, la cadena es "Camera".</span><span class="sxs-lookup"><span data-stu-id="8f7f4-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="8f7f4-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f7f4-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f7f4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f7f4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f7f4-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f7f4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f7f4-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="8f7f4-130">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="8f7f4-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f7f4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f7f4-131">Requirements</span></span>



| <span data-ttu-id="8f7f4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f7f4-132">Requirement</span></span> | <span data-ttu-id="8f7f4-133">Value</span><span class="sxs-lookup"><span data-stu-id="8f7f4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7f4-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f7f4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7f4-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f7f4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f7f4-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f7f4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7f4-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8f7f4-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8f7f4-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f7f4-138">Namespace</span></span><br/>                | <span data-ttu-id="8f7f4-139">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="8f7f4-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8f7f4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8f7f4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f7f4-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f7f4-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f7f4-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f7f4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f7f4-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f7f4-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7f4-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f7f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7f4-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="8f7f4-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

