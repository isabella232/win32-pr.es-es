---
title: MDM_ActiveSync_User_ContentTypes04_01 (clase)
description: La \_ \_ \_ clase ContentTypes04 01 de usuario \_ de MDM define el tipo de contenido que se va a habilitar o deshabilitar individualmente para la sincronización.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- MDM_ActiveSync_User_ContentTypes04_01 (clase)
- MDM_ActiveSync_User_ContentTypes04_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656524"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="8c625-105">\_ \_ \_ Clase ContentTypes04 01 de \_ usuario de MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="8c625-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="8c625-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="8c625-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c625-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="8c625-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c625-108">La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM** define el tipo de contenido que se va a habilitar o deshabilitar individualmente para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="8c625-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="8c625-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8c625-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c625-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c625-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8c625-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c625-111">Members</span></span>

<span data-ttu-id="8c625-112">La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM ActiveSync** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c625-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="8c625-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c625-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c625-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c625-114">Properties</span></span>

<span data-ttu-id="8c625-115">La **clase \_ \_ \_ ContentTypes04 \_ 01 de usuario de MDM ActiveSync** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c625-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c625-116">Enabled</span><span class="sxs-lookup"><span data-stu-id="8c625-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c625-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c625-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c625-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8c625-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c625-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c625-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c625-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c625-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c625-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c625-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c625-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c625-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c625-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8c625-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="8c625-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c625-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c625-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c625-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c625-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8c625-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c625-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8c625-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c625-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c625-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c625-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c625-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c625-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c625-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c625-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8c625-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="8c625-132">Para esta clase, la cadena es "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options".</span><span class="sxs-lookup"><span data-stu-id="8c625-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c625-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c625-133">Requirements</span></span>



| <span data-ttu-id="8c625-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c625-134">Requirement</span></span> | <span data-ttu-id="8c625-135">Value</span><span class="sxs-lookup"><span data-stu-id="8c625-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c625-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c625-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8c625-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c625-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c625-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c625-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8c625-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c625-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8c625-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c625-140">Namespace</span></span><br/>                | <span data-ttu-id="8c625-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="8c625-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8c625-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8c625-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c625-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c625-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c625-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c625-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c625-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c625-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c625-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c625-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c625-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="8c625-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

