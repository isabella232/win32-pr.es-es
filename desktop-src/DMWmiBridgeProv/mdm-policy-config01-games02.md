---
title: MDM_Policy_Config01_Games02 (clase)
description: La \_ clase Config01 de Games02 de directivas MDM \_ \_ configura los servicios de juegos avanzados.
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- MDM_Policy_Config01_Games02 (clase)
- MDM_Policy_Config01_Games02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079678"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="11b45-105">\_ \_ Clase Games02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="11b45-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="11b45-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="11b45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11b45-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="11b45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11b45-108">La \_ clase Config01 de Games02 de directivas MDM \_ \_ configura los servicios de juegos avanzados.</span><span class="sxs-lookup"><span data-stu-id="11b45-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="11b45-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="11b45-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b45-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11b45-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="11b45-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="11b45-111">Members</span></span>

<span data-ttu-id="11b45-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Games02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="11b45-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="11b45-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11b45-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11b45-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11b45-114">Properties</span></span>

<span data-ttu-id="11b45-115">La **clase \_ \_ Config01 de \_ Games02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="11b45-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11b45-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="11b45-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b45-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11b45-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11b45-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="11b45-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11b45-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11b45-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b45-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="11b45-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b45-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b45-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b45-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11b45-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11b45-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11b45-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b45-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="11b45-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b45-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11b45-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b45-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11b45-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11b45-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11b45-127">Requirements</span></span>



| <span data-ttu-id="11b45-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b45-128">Requirement</span></span> | <span data-ttu-id="11b45-129">Value</span><span class="sxs-lookup"><span data-stu-id="11b45-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b45-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11b45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="11b45-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="11b45-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11b45-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11b45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="11b45-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="11b45-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11b45-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="11b45-134">Namespace</span></span><br/>                | <span data-ttu-id="11b45-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="11b45-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11b45-136">MOF</span><span class="sxs-lookup"><span data-stu-id="11b45-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11b45-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11b45-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11b45-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11b45-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b45-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11b45-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

