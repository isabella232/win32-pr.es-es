---
title: MDM_AppLocker_CodeIntegrity03 (clase)
description: La \_ \_ clase CodeIntegrity03 de APPLOCKER de MDM define la Directiva de integridad de código.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- MDM_AppLocker_CodeIntegrity03 (clase)
- MDM_AppLocker_CodeIntegrity03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802053"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="eeeea-105">\_Clase CodeIntegrity03 de AppLocker de MDM \_</span><span class="sxs-lookup"><span data-stu-id="eeeea-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="eeeea-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="eeeea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eeeea-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="eeeea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eeeea-108">La **clase \_ \_ CodeIntegrity03 de AppLocker de MDM** define la Directiva de integridad de código.</span><span class="sxs-lookup"><span data-stu-id="eeeea-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="eeeea-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eeeea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeeea-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeeea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="eeeea-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="eeeea-111">Members</span></span>

<span data-ttu-id="eeeea-112">La **clase \_ \_ CodeIntegrity03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eeeea-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="eeeea-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeeea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eeeea-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeeea-114">Properties</span></span>

<span data-ttu-id="eeeea-115">La **clase \_ \_ CodeIntegrity03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eeeea-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeeea-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eeeea-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeeea-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeeea-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eeeea-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eeeea-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eeeea-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="eeeea-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="eeeea-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eeeea-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeeea-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeeea-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eeeea-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eeeea-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eeeea-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="eeeea-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="eeeea-126">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="eeeea-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="eeeea-127">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="eeeea-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeeea-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeeea-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eeeea-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eeeea-130">Calificadores: **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="eeeea-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eeeea-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeeea-131">Requirements</span></span>



| <span data-ttu-id="eeeea-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeeea-132">Requirement</span></span> | <span data-ttu-id="eeeea-133">Value</span><span class="sxs-lookup"><span data-stu-id="eeeea-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeea-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeeea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eeeea-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="eeeea-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eeeea-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeeea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eeeea-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eeeea-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eeeea-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eeeea-138">Namespace</span></span><br/>                | <span data-ttu-id="eeeea-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="eeeea-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eeeea-140">MOF</span><span class="sxs-lookup"><span data-stu-id="eeeea-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeeea-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeeea-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeeea-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeeea-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeeea-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeeea-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeeea-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeeea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeeea-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="eeeea-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

