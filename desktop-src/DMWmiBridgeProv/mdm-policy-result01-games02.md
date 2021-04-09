---
title: MDM_Policy_Result01_Games02 (clase)
description: La \_ \_ \_ clase Result01 de GAMES02 de directivas MDM obtiene la configuración de los servicios de juegos avanzados.
ms.assetid: c8d17de7-b645-4937-af9f-94bfc039b2fc
keywords:
- MDM_Policy_Result01_Games02 (clase)
- MDM_Policy_Result01_Games02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Games02
- MDM_Policy_Result01_Games02.InstanceID
- MDM_Policy_Result01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a0a9a216b8bb2610e25ffdbd4e233fc8b3f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150400"
---
# <a name="mdm_policy_result01_games02-class"></a><span data-ttu-id="35bbc-105">\_ \_ Clase Games02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="35bbc-105">MDM\_Policy\_Result01\_Games02 class</span></span>

<span data-ttu-id="35bbc-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="35bbc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="35bbc-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="35bbc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="35bbc-108">La \_ \_ \_ clase Result01 de GAMES02 de directivas MDM obtiene la configuración de los servicios de juegos avanzados.</span><span class="sxs-lookup"><span data-stu-id="35bbc-108">The MDM\_Policy\_Result01\_Games02 class gets the settings of the advanced gaming services.</span></span>

<span data-ttu-id="35bbc-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35bbc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35bbc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35bbc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="35bbc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="35bbc-111">Members</span></span>

<span data-ttu-id="35bbc-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Games02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35bbc-112">The **MDM\_Policy\_Result01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="35bbc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35bbc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35bbc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35bbc-114">Properties</span></span>

<span data-ttu-id="35bbc-115">La **clase \_ \_ Result01 de \_ Games02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35bbc-115">The **MDM\_Policy\_Result01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="35bbc-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="35bbc-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35bbc-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="35bbc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="35bbc-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35bbc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35bbc-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35bbc-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35bbc-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35bbc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35bbc-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35bbc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35bbc-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35bbc-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35bbc-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="35bbc-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35bbc-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35bbc-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35bbc-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35bbc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35bbc-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35bbc-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35bbc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35bbc-127">Requirements</span></span>



| <span data-ttu-id="35bbc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="35bbc-128">Requirement</span></span> | <span data-ttu-id="35bbc-129">Value</span><span class="sxs-lookup"><span data-stu-id="35bbc-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35bbc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35bbc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35bbc-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="35bbc-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35bbc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35bbc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35bbc-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35bbc-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="35bbc-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35bbc-134">Namespace</span></span><br/>                | <span data-ttu-id="35bbc-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="35bbc-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="35bbc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="35bbc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35bbc-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35bbc-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="35bbc-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35bbc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35bbc-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35bbc-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

