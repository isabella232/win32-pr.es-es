---
title: MDM_Policy_Result01_Location02 (clase)
description: La \_ clase Result01 de Location02 de directivas MDM \_ \_ obtiene los valores del servicio de ubicación del dispositivo.
ms.assetid: f6d639db-c9d4-4d7e-b857-54aad602ea29
keywords:
- MDM_Policy_Result01_Location02 (clase)
- MDM_Policy_Result01_Location02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Location02
- MDM_Policy_Result01_Location02.InstanceID
- MDM_Policy_Result01_Location02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 210fb38e45e600e45590acecb9c647d00ab13995
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905166"
---
# <a name="mdm_policy_result01_location02-class"></a><span data-ttu-id="9a1eb-105">\_ \_ Clase Location02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="9a1eb-105">MDM\_Policy\_Result01\_Location02 class</span></span>

<span data-ttu-id="9a1eb-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9a1eb-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9a1eb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9a1eb-108">La \_ clase Result01 de Location02 de directivas MDM \_ \_ obtiene los valores del servicio de ubicación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-108">The MDM\_Policy\_Result01\_Location02 class gets the settings of the location service of the device.</span></span>

<span data-ttu-id="9a1eb-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1eb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a1eb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Location02
{
  string InstanceID;
  string ParentID;
  sint32 EnableLocation;
};
```

## <a name="members"></a><span data-ttu-id="9a1eb-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a1eb-111">Members</span></span>

<span data-ttu-id="9a1eb-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Location02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a1eb-112">The **MDM\_Policy\_Result01\_Location02** class has these types of members:</span></span>

-   [<span data-ttu-id="9a1eb-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a1eb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a1eb-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a1eb-114">Properties</span></span>

<span data-ttu-id="9a1eb-115">La **clase \_ \_ Result01 de \_ Location02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-115">The **MDM\_Policy\_Result01\_Location02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a1eb-116">**EnableLocation**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-116">**EnableLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a1eb-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a1eb-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a1eb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9a1eb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a1eb-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a1eb-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a1eb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a1eb-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a1eb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9a1eb-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a1eb-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a1eb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a1eb-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a1eb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a1eb-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a1eb-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a1eb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a1eb-127">Requirements</span></span>



| <span data-ttu-id="9a1eb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a1eb-128">Requirement</span></span> | <span data-ttu-id="9a1eb-129">Value</span><span class="sxs-lookup"><span data-stu-id="9a1eb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1eb-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a1eb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1eb-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a1eb-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a1eb-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a1eb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1eb-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9a1eb-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9a1eb-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a1eb-134">Namespace</span></span><br/>                | <span data-ttu-id="9a1eb-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9a1eb-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9a1eb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9a1eb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a1eb-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a1eb-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a1eb-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a1eb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a1eb-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a1eb-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

