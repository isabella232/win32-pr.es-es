---
title: MDM_ActiveSync_User_Options03 (clase)
description: La \_ \_ clase Options03 de usuario de MDM ActiveSync \_ define las opciones que se establecen para cada cuenta de ActiveSync.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- MDM_ActiveSync_User_Options03 (clase)
- MDM_ActiveSync_User_Options03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150182"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="d1d51-105">\_ \_ Clase Options03 de usuario de MDM ActiveSync \_</span><span class="sxs-lookup"><span data-stu-id="d1d51-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="d1d51-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d1d51-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d1d51-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d1d51-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d1d51-108">La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** define las opciones que se establecen para cada cuenta de ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="d1d51-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="d1d51-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d1d51-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d51-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1d51-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="d1d51-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1d51-111">Members</span></span>

<span data-ttu-id="d1d51-112">La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1d51-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="d1d51-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1d51-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1d51-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1d51-114">Properties</span></span>

<span data-ttu-id="d1d51-115">La **clase \_ \_ \_ Options03 de usuario de MDM ActiveSync** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1d51-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1d51-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1d51-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1d51-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1d51-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1d51-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d1d51-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="d1d51-121">Logging</span><span class="sxs-lookup"><span data-stu-id="d1d51-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1d51-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1d51-124">MailAgeFilter</span><span class="sxs-lookup"><span data-stu-id="d1d51-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1d51-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1d51-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d1d51-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1d51-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1d51-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1d51-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d1d51-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="d1d51-132">Para esta clase, la cadena es "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span><span class="sxs-lookup"><span data-stu-id="d1d51-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="d1d51-133">Programación</span><span class="sxs-lookup"><span data-stu-id="d1d51-133">Schedule</span></span>](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1d51-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1d51-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="d1d51-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1d51-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1d51-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1d51-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d1d51-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1d51-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d51-139">Requirements</span></span>



| <span data-ttu-id="d1d51-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d51-140">Requirement</span></span> | <span data-ttu-id="d1d51-141">Value</span><span class="sxs-lookup"><span data-stu-id="d1d51-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d51-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d51-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d51-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1d51-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1d51-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d51-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d51-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1d51-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d1d51-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1d51-146">Namespace</span></span><br/>                | <span data-ttu-id="d1d51-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d1d51-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d1d51-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d1d51-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1d51-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1d51-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1d51-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1d51-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d51-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1d51-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d51-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1d51-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d51-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="d1d51-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

