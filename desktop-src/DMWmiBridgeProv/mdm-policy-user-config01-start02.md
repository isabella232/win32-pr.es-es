---
title: MDM_Policy_User_Config01_Start02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Start02 representa las directivas de inicio disponibles que se establecen por usuario.
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- MDM_Policy_User_Config01_Start02 (clase)
- MDM_Policy_User_Config01_Start02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422345"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="21148-105">\_Clase Start02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="21148-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="21148-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="21148-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="21148-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="21148-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="21148-108">La **clase \_ Config01 de usuario de directiva de MDM \_ \_ \_ Start02** representa las directivas de inicio disponibles que se establecen por usuario.</span><span class="sxs-lookup"><span data-stu-id="21148-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="21148-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="21148-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="21148-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21148-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="21148-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="21148-111">Members</span></span>

<span data-ttu-id="21148-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Start02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="21148-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="21148-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="21148-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21148-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="21148-114">Properties</span></span>

<span data-ttu-id="21148-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Start02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="21148-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="21148-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="21148-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21148-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="21148-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21148-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="21148-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="21148-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="21148-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21148-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="21148-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21148-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="21148-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21148-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21148-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="21148-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="21148-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="21148-124">Para esta clase, la cadena es "Start".</span><span class="sxs-lookup"><span data-stu-id="21148-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="21148-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="21148-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21148-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="21148-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21148-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="21148-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21148-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21148-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="21148-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="21148-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="21148-130">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="21148-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="21148-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="21148-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21148-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="21148-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21148-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="21148-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21148-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21148-134">Requirements</span></span>



| <span data-ttu-id="21148-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="21148-135">Requirement</span></span> | <span data-ttu-id="21148-136">Value</span><span class="sxs-lookup"><span data-stu-id="21148-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21148-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21148-137">Minimum supported client</span></span><br/> | <span data-ttu-id="21148-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="21148-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21148-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21148-139">Minimum supported server</span></span><br/> | <span data-ttu-id="21148-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="21148-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="21148-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21148-141">Namespace</span></span><br/>                | <span data-ttu-id="21148-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="21148-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="21148-143">MOF</span><span class="sxs-lookup"><span data-stu-id="21148-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21148-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21148-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="21148-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21148-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21148-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21148-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21148-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="21148-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21148-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="21148-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

