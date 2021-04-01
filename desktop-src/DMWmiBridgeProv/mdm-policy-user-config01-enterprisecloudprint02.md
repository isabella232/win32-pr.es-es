---
title: MDM_Policy_User_Config01_EnterpriseCloudPrint02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ EnterpriseCloudPrint02 representa las directivas de impresión en la nube disponibles.
ms.assetid: cc885184-1197-48c4-ba48-a2944a416534
keywords:
- MDM_Policy_User_Config01_EnterpriseCloudPrint02 (clase)
- MDM_Policy_User_Config01_EnterpriseCloudPrint02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_EnterpriseCloudPrint02
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2b9d42afbab4d3f17d91b6db630ef67faf6ccc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905274"
---
# <a name="mdm_policy_user_config01_enterprisecloudprint02-class"></a><span data-ttu-id="39421-105">\_Clase EnterpriseCloudPrint02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="39421-105">MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="39421-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="39421-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="39421-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="39421-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="39421-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ EnterpriseCloudPrint02 representa las directivas de impresión en la nube disponibles.</span><span class="sxs-lookup"><span data-stu-id="39421-108">The MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="39421-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="39421-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39421-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39421-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="39421-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="39421-111">Members</span></span>

<span data-ttu-id="39421-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ EnterpriseCloudPrint02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39421-112">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="39421-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39421-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39421-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39421-114">Properties</span></span>

<span data-ttu-id="39421-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ EnterpriseCloudPrint02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="39421-115">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="39421-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="39421-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39421-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="39421-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39421-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="39421-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39421-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="39421-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39421-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="39421-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39421-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39421-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39421-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39421-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39421-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39421-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39421-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39421-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="39421-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="39421-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39421-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="39421-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39421-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39421-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39421-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39421-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39421-141">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39421-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39421-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39421-142">Requirements</span></span>



| <span data-ttu-id="39421-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="39421-143">Requirement</span></span> | <span data-ttu-id="39421-144">Value</span><span class="sxs-lookup"><span data-stu-id="39421-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39421-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39421-145">Minimum supported client</span></span><br/> | <span data-ttu-id="39421-146">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="39421-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39421-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39421-147">Minimum supported server</span></span><br/> | <span data-ttu-id="39421-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="39421-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="39421-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39421-149">Namespace</span></span><br/>                | <span data-ttu-id="39421-150">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="39421-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="39421-151">MOF</span><span class="sxs-lookup"><span data-stu-id="39421-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39421-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39421-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="39421-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39421-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39421-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39421-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

