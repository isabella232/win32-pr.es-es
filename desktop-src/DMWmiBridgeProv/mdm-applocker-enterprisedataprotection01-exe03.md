---
title: MDM_AppLocker_EnterpriseDataProtection01_EXE03 (clase)
description: La \_ \_ \_ clase EnterpriseDataProtection01 EXE03 de AppLocker de MDM captura la lista de aplicaciones ejecutables que pueden administrar los datos empresariales.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 (clase)
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151109"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="9b5b8-105">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ clase EXE03</span><span class="sxs-lookup"><span data-stu-id="9b5b8-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="9b5b8-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9b5b8-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9b5b8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9b5b8-108">La **clase \_ \_ EnterpriseDataProtection01 \_ EXE03 de AppLocker de MDM** captura la lista de aplicaciones ejecutables que pueden administrar los datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="9b5b8-109">Debe utilizarse junto con la configuración de./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="9b5b8-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b5b8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b5b8-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="9b5b8-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b5b8-112">Members</span></span>

<span data-ttu-id="9b5b8-113">La **clase \_ \_ EnterpriseDataProtection01 de \_ EXE03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b5b8-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="9b5b8-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b5b8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b5b8-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b5b8-115">Properties</span></span>

<span data-ttu-id="9b5b8-116">La **clase \_ \_ EnterpriseDataProtection01 \_ EXE03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b5b8-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b5b8-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b5b8-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b5b8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b5b8-120">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b5b8-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b5b8-121">Define las restricciones para iniciar aplicaciones ejecutables.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="9b5b8-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b5b8-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b5b8-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b5b8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b5b8-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b5b8-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b5b8-126">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="9b5b8-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="9b5b8-127">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*".</span><span class="sxs-lookup"><span data-stu-id="9b5b8-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="9b5b8-128">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b5b8-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b5b8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b5b8-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9b5b8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b5b8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b5b8-131">Requirements</span></span>



| <span data-ttu-id="9b5b8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b5b8-132">Requirement</span></span> | <span data-ttu-id="9b5b8-133">Value</span><span class="sxs-lookup"><span data-stu-id="9b5b8-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5b8-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b5b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9b5b8-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b5b8-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b5b8-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b5b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9b5b8-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b5b8-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9b5b8-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b5b8-138">Namespace</span></span><br/>                | <span data-ttu-id="9b5b8-139">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9b5b8-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9b5b8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9b5b8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b5b8-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b5b8-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b5b8-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b5b8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b5b8-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b5b8-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b5b8-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b5b8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b5b8-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="9b5b8-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

