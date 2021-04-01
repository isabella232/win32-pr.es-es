---
title: MDM_PassportForWork_Device_Policies02 (clase)
description: La \_ \_ clase Policies02 del dispositivo MDM PassportForWork \_ define la configuración de la Directiva de Windows Hello para empresas.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- MDM_PassportForWork_Device_Policies02 (clase)
- MDM_PassportForWork_Device_Policies02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996201"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="09e49-105">\_ \_ Clase Policies02 de dispositivo PASSPORTFORWORK de MDM \_</span><span class="sxs-lookup"><span data-stu-id="09e49-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="09e49-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="09e49-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="09e49-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="09e49-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="09e49-108">La **clase \_ \_ \_ Policies02 del dispositivo MDM PassportForWork** define la configuración de la Directiva de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="09e49-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="09e49-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="09e49-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e49-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09e49-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="09e49-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="09e49-111">Members</span></span>

<span data-ttu-id="09e49-112">La **clase \_ \_ \_ Policies02 del dispositivo PassportForWork de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="09e49-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="09e49-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09e49-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09e49-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09e49-114">Properties</span></span>

<span data-ttu-id="09e49-115">La **clase \_ \_ \_ Policies02 del dispositivo PassportForWork de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="09e49-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09e49-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09e49-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e49-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09e49-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e49-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09e49-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09e49-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09e49-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09e49-120">Nodo para la configuración de la Directiva de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="09e49-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="09e49-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="09e49-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e49-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="09e49-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09e49-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09e49-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09e49-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09e49-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09e49-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="09e49-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="09e49-126">Para esta clase, la cadena es "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span><span class="sxs-lookup"><span data-stu-id="09e49-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="09e49-127">UseCertificateForOnPremAuth</span><span class="sxs-lookup"><span data-stu-id="09e49-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09e49-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="09e49-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09e49-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09e49-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09e49-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e49-130">Requirements</span></span>



| <span data-ttu-id="09e49-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e49-131">Requirement</span></span> | <span data-ttu-id="09e49-132">Value</span><span class="sxs-lookup"><span data-stu-id="09e49-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e49-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e49-133">Minimum supported client</span></span><br/> | <span data-ttu-id="09e49-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="09e49-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09e49-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09e49-135">Minimum supported server</span></span><br/> | <span data-ttu-id="09e49-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="09e49-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="09e49-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09e49-137">Namespace</span></span><br/>                | <span data-ttu-id="09e49-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="09e49-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="09e49-139">MOF</span><span class="sxs-lookup"><span data-stu-id="09e49-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09e49-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09e49-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="09e49-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09e49-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e49-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e49-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

