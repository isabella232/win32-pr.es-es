---
title: MDM_VPNv2_Eap04 (clase)
description: La \_ clase Eap04 de VPNv2 de MDM \_ contiene la información XML de configuración necesaria cuando el perfil nativo especifica la autenticación EAP.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- MDM_VPNv2_Eap04 (clase)
- MDM_VPNv2_Eap04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803523"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="7e91a-105">\_Clase Eap04 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="7e91a-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="7e91a-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7e91a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7e91a-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7e91a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7e91a-108">La **clase \_ \_ Eap04 de VPNv2 de MDM** contiene la información XML de configuración necesaria cuando el perfil nativo especifica la autenticación EAP.</span><span class="sxs-lookup"><span data-stu-id="7e91a-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="7e91a-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7e91a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e91a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e91a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="7e91a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e91a-111">Members</span></span>

<span data-ttu-id="7e91a-112">La **clase \_ \_ Eap04 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e91a-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="7e91a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e91a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e91a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e91a-114">Properties</span></span>

<span data-ttu-id="7e91a-115">La **clase \_ \_ Eap04 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e91a-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7e91a-116">Configuración</span><span class="sxs-lookup"><span data-stu-id="7e91a-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e91a-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e91a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e91a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e91a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e91a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e91a-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e91a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e91a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e91a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e91a-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7e91a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="7e91a-124">Para esta clase, la cadena es "EAP"</span><span class="sxs-lookup"><span data-stu-id="7e91a-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="7e91a-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7e91a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e91a-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e91a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e91a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e91a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e91a-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7e91a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="7e91a-130">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="7e91a-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="7e91a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e91a-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e91a-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e91a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e91a-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e91a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e91a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e91a-134">Requirements</span></span>



| <span data-ttu-id="7e91a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e91a-135">Requirement</span></span> | <span data-ttu-id="7e91a-136">Value</span><span class="sxs-lookup"><span data-stu-id="7e91a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e91a-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e91a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7e91a-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e91a-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e91a-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e91a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7e91a-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7e91a-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7e91a-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e91a-141">Namespace</span></span><br/>                | <span data-ttu-id="7e91a-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7e91a-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7e91a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7e91a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e91a-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e91a-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e91a-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e91a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e91a-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e91a-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e91a-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e91a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e91a-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="7e91a-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

