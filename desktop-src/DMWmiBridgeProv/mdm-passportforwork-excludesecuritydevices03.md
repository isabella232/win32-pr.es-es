---
title: MDM_PassportForWork_ExcludeSecurityDevices03 (clase)
description: La \_ clase ExcludeSecurityDevices03 de MDM PassportForWork \_ define los módulos de plataforma segura que se pueden usar con Windows Hello para empresas.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- MDM_PassportForWork_ExcludeSecurityDevices03 (clase)
- MDM_PassportForWork_ExcludeSecurityDevices03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079191"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="7ca1f-105">\_Clase ExcludeSecurityDevices03 PassportForWork de MDM \_</span><span class="sxs-lookup"><span data-stu-id="7ca1f-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="7ca1f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ca1f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7ca1f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ca1f-108">La \_ clase ExcludeSecurityDevices03 de MDM PassportForWork \_ define los módulos de plataforma segura que se pueden usar con Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="7ca1f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca1f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ca1f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="7ca1f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ca1f-111">Members</span></span>

<span data-ttu-id="7ca1f-112">La **clase \_ \_ ExcludeSecurityDevices03 de MDM PassportForWork** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7ca1f-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="7ca1f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ca1f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ca1f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ca1f-114">Properties</span></span>

<span data-ttu-id="7ca1f-115">La **clase \_ \_ ExcludeSecurityDevices03 de MDM PassportForWork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ca1f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ca1f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca1f-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ca1f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca1f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ca1f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca1f-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ca1f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ca1f-120">Nodo raíz:</span><span class="sxs-lookup"><span data-stu-id="7ca1f-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="7ca1f-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7ca1f-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca1f-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7ca1f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca1f-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ca1f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca1f-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ca1f-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ca1f-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="7ca1f-126">Para obtener más información, consulte [PASSPORTFORWORK CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ca1f-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="7ca1f-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca1f-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7ca1f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ca1f-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7ca1f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ca1f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ca1f-130">Requirements</span></span>



| <span data-ttu-id="7ca1f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca1f-131">Requirement</span></span> | <span data-ttu-id="7ca1f-132">Value</span><span class="sxs-lookup"><span data-stu-id="7ca1f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca1f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ca1f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca1f-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ca1f-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ca1f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ca1f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca1f-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7ca1f-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ca1f-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7ca1f-137">Namespace</span></span><br/>                | <span data-ttu-id="7ca1f-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7ca1f-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7ca1f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7ca1f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ca1f-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ca1f-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ca1f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ca1f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ca1f-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ca1f-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

