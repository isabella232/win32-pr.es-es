---
title: MDM_ActiveSync_User_Accounts01_01 (clase)
description: La \_ \_ clase Accounts01 01 de usuario de MDM \_ \_ define todas las cuentas de ActiveSync disponibles.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- MDM_ActiveSync_User_Accounts01_01 (clase)
- MDM_ActiveSync_User_Accounts01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490180"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="a22d3-105">\_ \_ \_ Clase Accounts01 01 de \_ usuario de MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="a22d3-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="a22d3-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a22d3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a22d3-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a22d3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a22d3-108">La **clase \_ \_ \_ Accounts01 \_ 01 de usuario de MDM** define todas las cuentas de ActiveSync disponibles.</span><span class="sxs-lookup"><span data-stu-id="a22d3-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="a22d3-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a22d3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22d3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22d3-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="a22d3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a22d3-111">Members</span></span>

<span data-ttu-id="a22d3-112">La **clase \_ \_ \_ Accounts01 \_ 01 de usuario de MDM ActiveSync** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a22d3-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a22d3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a22d3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a22d3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a22d3-114">Properties</span></span>

<span data-ttu-id="a22d3-115">La **clase \_ \_ \_ Accounts01 \_ 01 de usuario de MDM ActiveSync** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a22d3-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a22d3-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="a22d3-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="a22d3-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="a22d3-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="a22d3-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a22d3-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22d3-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a22d3-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a22d3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a22d3-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a22d3-135">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a22d3-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="a22d3-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a22d3-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a22d3-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a22d3-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a22d3-140">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a22d3-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="a22d3-141">Para esta clase, la cadena es "./Vendor/MSFT/ActiveSync/".</span><span class="sxs-lookup"><span data-stu-id="a22d3-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="a22d3-142">Contraseña</span><span class="sxs-lookup"><span data-stu-id="a22d3-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="a22d3-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22d3-148">UserName</span><span class="sxs-lookup"><span data-stu-id="a22d3-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d3-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a22d3-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22d3-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a22d3-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a22d3-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22d3-151">Requirements</span></span>



| <span data-ttu-id="a22d3-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22d3-152">Requirement</span></span> | <span data-ttu-id="a22d3-153">Value</span><span class="sxs-lookup"><span data-stu-id="a22d3-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22d3-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22d3-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a22d3-155">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a22d3-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a22d3-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22d3-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a22d3-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a22d3-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a22d3-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a22d3-158">Namespace</span></span><br/>                | <span data-ttu-id="a22d3-159">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a22d3-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a22d3-160">MOF</span><span class="sxs-lookup"><span data-stu-id="a22d3-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22d3-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a22d3-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a22d3-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a22d3-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22d3-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22d3-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22d3-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="a22d3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22d3-165">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="a22d3-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

