---
title: MDM_EnterpriseAPN_01 (clase)
description: '\_ \_ La empresa utiliza la clase de ENTERPRISEAPN de MDM 01 para aprovisionar un APN para Internet.'
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- MDM_EnterpriseAPN_01 (clase)
- MDM_EnterpriseAPN_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274531"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="71fc6-105">Clase de EnterpriseAPN de MDM \_ \_ 01</span><span class="sxs-lookup"><span data-stu-id="71fc6-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="71fc6-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="71fc6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="71fc6-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="71fc6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="71fc6-108">La empresa utiliza la clase de **EnterpriseAPN de MDM \_ \_ 01** para aprovisionar un APN para Internet.</span><span class="sxs-lookup"><span data-stu-id="71fc6-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="71fc6-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="71fc6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71fc6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71fc6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="71fc6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="71fc6-111">Members</span></span>

<span data-ttu-id="71fc6-112">La **clase \_ EnterpriseAPN \_ de MDM 01** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="71fc6-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="71fc6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71fc6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71fc6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71fc6-114">Properties</span></span>

<span data-ttu-id="71fc6-115">La clase de **EnterpriseAPN de MDM \_ \_ 01** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71fc6-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="71fc6-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="71fc6-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71fc6-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-119">APNName</span><span class="sxs-lookup"><span data-stu-id="71fc6-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="71fc6-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-125">ClassId</span><span class="sxs-lookup"><span data-stu-id="71fc6-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="71fc6-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71fc6-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-131">IccId</span><span class="sxs-lookup"><span data-stu-id="71fc6-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71fc6-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="71fc6-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71fc6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71fc6-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71fc6-138">Nombre de la conexión tal como la ha detectado el administrador de conexiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="71fc6-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="71fc6-139">IPType</span><span class="sxs-lookup"><span data-stu-id="71fc6-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="71fc6-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="71fc6-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71fc6-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="71fc6-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71fc6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-148">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71fc6-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71fc6-149">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="71fc6-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="71fc6-150">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseAPN".</span><span class="sxs-lookup"><span data-stu-id="71fc6-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="71fc6-151">Contraseña</span><span class="sxs-lookup"><span data-stu-id="71fc6-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-154">Móviles</span><span class="sxs-lookup"><span data-stu-id="71fc6-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71fc6-157">UserName</span><span class="sxs-lookup"><span data-stu-id="71fc6-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fc6-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="71fc6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fc6-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="71fc6-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71fc6-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71fc6-160">Requirements</span></span>



| <span data-ttu-id="71fc6-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="71fc6-161">Requirement</span></span> | <span data-ttu-id="71fc6-162">Value</span><span class="sxs-lookup"><span data-stu-id="71fc6-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71fc6-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71fc6-163">Minimum supported client</span></span><br/> | <span data-ttu-id="71fc6-164">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="71fc6-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71fc6-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71fc6-165">Minimum supported server</span></span><br/> | <span data-ttu-id="71fc6-166">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="71fc6-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="71fc6-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71fc6-167">Namespace</span></span><br/>                | <span data-ttu-id="71fc6-168">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="71fc6-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="71fc6-169">MOF</span><span class="sxs-lookup"><span data-stu-id="71fc6-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71fc6-170"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71fc6-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="71fc6-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71fc6-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71fc6-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71fc6-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71fc6-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="71fc6-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fc6-174">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="71fc6-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

