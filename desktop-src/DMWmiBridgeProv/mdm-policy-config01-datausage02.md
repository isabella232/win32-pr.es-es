---
title: MDM_Policy_Config01_DataUsage02 (clase)
description: La \_ clase Config01 de DataUsage02 de directivas MDM \_ \_ configura las directivas de uso de datos disponibles.
ms.assetid: c5e77d82-df5e-4eed-90f5-50f2ed62e975
keywords:
- MDM_Policy_Config01_DataUsage02 (clase)
- MDM_Policy_Config01_DataUsage02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataUsage02
- MDM_Policy_Config01_DataUsage02.InstanceID
- MDM_Policy_Config01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b878ec3bf38444dd82c08fe880e84028067bbd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150109"
---
# <a name="mdm_policy_config01_datausage02-class"></a><span data-ttu-id="f8506-105">\_ \_ Clase DataUsage02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="f8506-105">MDM\_Policy\_Config01\_DataUsage02 class</span></span>

<span data-ttu-id="f8506-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f8506-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f8506-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f8506-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f8506-108">La \_ clase Config01 de DataUsage02 de directivas MDM \_ \_ configura las directivas de uso de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f8506-108">The MDM\_Policy\_Config01\_DataUsage02 class configures the available data usage policies.</span></span>

<span data-ttu-id="f8506-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f8506-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8506-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8506-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="f8506-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8506-111">Members</span></span>

<span data-ttu-id="f8506-112">La clase Config01 de la **\_ Directiva MDM \_ \_ DataUsage02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f8506-112">The **MDM\_Policy\_Config01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="f8506-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8506-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8506-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8506-114">Properties</span></span>

<span data-ttu-id="f8506-115">La **clase \_ \_ Config01 de \_ DataUsage02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8506-115">The **MDM\_Policy\_Config01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8506-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f8506-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8506-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f8506-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8506-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f8506-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8506-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8506-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8506-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f8506-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8506-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f8506-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8506-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f8506-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8506-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8506-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f8506-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="f8506-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8506-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f8506-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8506-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f8506-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f8506-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="f8506-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8506-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f8506-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8506-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f8506-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8506-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8506-130">Requirements</span></span>



| <span data-ttu-id="f8506-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8506-131">Requirement</span></span> | <span data-ttu-id="f8506-132">Value</span><span class="sxs-lookup"><span data-stu-id="f8506-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8506-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8506-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8506-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8506-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8506-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8506-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8506-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f8506-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f8506-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8506-137">Namespace</span></span><br/>                | <span data-ttu-id="f8506-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f8506-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f8506-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f8506-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8506-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8506-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8506-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8506-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8506-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8506-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

