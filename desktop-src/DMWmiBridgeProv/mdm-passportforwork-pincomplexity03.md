---
title: MDM_PassportForWork_PINComplexity03 (clase)
description: La \_ clase PINComplexity03 de MDM PassportForWork \_ define la complejidad del PIN para las credenciales de inicio de sesión de Windows Hello para empresas.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- MDM_PassportForWork_PINComplexity03 (clase)
- MDM_PassportForWork_PINComplexity03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996199"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="f2783-105">\_Clase PINComplexity03 PassportForWork de MDM \_</span><span class="sxs-lookup"><span data-stu-id="f2783-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="f2783-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f2783-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2783-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f2783-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2783-108">La **clase \_ \_ PINComplexity03 de MDM PassportForWork** define la complejidad del PIN para las credenciales de inicio de sesión de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="f2783-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="f2783-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f2783-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2783-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2783-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="f2783-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2783-111">Members</span></span>

<span data-ttu-id="f2783-112">La **clase \_ \_ PINComplexity03 de MDM PassportForWork** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f2783-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="f2783-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2783-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2783-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2783-114">Properties</span></span>

<span data-ttu-id="f2783-115">La **clase \_ \_ PINComplexity03 de MDM PassportForWork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2783-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f2783-116">Anual</span><span class="sxs-lookup"><span data-stu-id="f2783-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2783-119">Expiración</span><span class="sxs-lookup"><span data-stu-id="f2783-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2783-122">Historial</span><span class="sxs-lookup"><span data-stu-id="f2783-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2783-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2783-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2783-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2783-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2783-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2783-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2783-129">Nodo raíz para las directivas de PIN.</span><span class="sxs-lookup"><span data-stu-id="f2783-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="f2783-130">LowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="f2783-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2783-133">MaximumPINLength</span><span class="sxs-lookup"><span data-stu-id="f2783-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-134">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2783-136">MinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="f2783-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-137">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2783-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2783-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f2783-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2783-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2783-142">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2783-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2783-143">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f2783-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2783-144">Para esta clase, la cadena es "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies".</span><span class="sxs-lookup"><span data-stu-id="f2783-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="f2783-145">SpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="f2783-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-146">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2783-148">UppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="f2783-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2783-149">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f2783-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2783-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f2783-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2783-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2783-151">Requirements</span></span>



| <span data-ttu-id="f2783-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2783-152">Requirement</span></span> | <span data-ttu-id="f2783-153">Value</span><span class="sxs-lookup"><span data-stu-id="f2783-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2783-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2783-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f2783-155">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2783-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2783-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2783-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f2783-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f2783-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2783-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2783-158">Namespace</span></span><br/>                | <span data-ttu-id="f2783-159">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f2783-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f2783-160">MOF</span><span class="sxs-lookup"><span data-stu-id="f2783-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2783-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2783-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2783-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2783-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2783-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2783-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2783-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2783-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2783-165">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="f2783-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

