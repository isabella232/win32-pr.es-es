---
title: MDM_PassportForWork (clase)
description: La PassportForWork de MDM \_ se usa para aprovisionar Windows Hello para empresas.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- MDM_PassportForWork (clase)
- MDM_PassportForWork clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079187"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="9ae70-105">\_Clase PassportForWork de MDM</span><span class="sxs-lookup"><span data-stu-id="9ae70-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="9ae70-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9ae70-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9ae70-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9ae70-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9ae70-108">La **\_ PassportForWork de MDM** se usa para aprovisionar Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="9ae70-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="9ae70-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9ae70-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae70-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ae70-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="9ae70-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ae70-111">Members</span></span>

<span data-ttu-id="9ae70-112">La **clase \_ PassportForWork de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9ae70-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="9ae70-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ae70-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ae70-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ae70-114">Properties</span></span>

<span data-ttu-id="9ae70-115">La **clase \_ PassportForWork de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9ae70-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ae70-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9ae70-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae70-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ae70-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae70-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ae70-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae70-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ae70-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ae70-120">Especifica el identificador de inquilino en el formato de un identificador único global (GUID) sin llaves ({,}), que se usará como parte del aprovisionamiento y la administración de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="9ae70-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="9ae70-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9ae70-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae70-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9ae70-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae70-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ae70-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae70-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ae70-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ae70-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="9ae70-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="9ae70-126">Para esta clase, la cadena es "./Vendor/MSFT/PassPortForWork/".</span><span class="sxs-lookup"><span data-stu-id="9ae70-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="9ae70-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="9ae70-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae70-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9ae70-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ae70-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9ae70-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ae70-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae70-130">Requirements</span></span>



| <span data-ttu-id="9ae70-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae70-131">Requirement</span></span> | <span data-ttu-id="9ae70-132">Value</span><span class="sxs-lookup"><span data-stu-id="9ae70-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae70-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae70-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae70-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ae70-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ae70-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ae70-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae70-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9ae70-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9ae70-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9ae70-137">Namespace</span></span><br/>                | <span data-ttu-id="9ae70-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9ae70-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9ae70-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9ae70-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ae70-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ae70-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ae70-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ae70-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae70-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae70-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae70-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ae70-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae70-144">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="9ae70-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

