---
title: MDM_WindowsLicensing_Subscriptions01_01 (clase)
description: La \_ clase MDM WindowsLicensing \_ Subscriptions01 \_ 01 está diseñada para escenarios de administración de licencias relacionados con la suscripción.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- MDM_WindowsLicensing_Subscriptions01_01 (clase)
- MDM_WindowsLicensing_Subscriptions01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150705"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="2eb03-105">\_Clase WindowsLicensing \_ Subscriptions01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="2eb03-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="2eb03-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2eb03-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2eb03-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2eb03-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2eb03-108">La clase **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** está diseñada para escenarios de administración de licencias relacionados con la suscripción.</span><span class="sxs-lookup"><span data-stu-id="2eb03-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="2eb03-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2eb03-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb03-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eb03-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2eb03-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2eb03-111">Members</span></span>

<span data-ttu-id="2eb03-112">La **clase \_ WindowsLicensing \_ Subscriptions01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2eb03-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2eb03-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2eb03-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2eb03-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2eb03-114">Properties</span></span>

<span data-ttu-id="2eb03-115">La **clase \_ WindowsLicensing \_ Subscriptions01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2eb03-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2eb03-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2eb03-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb03-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2eb03-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2eb03-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2eb03-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2eb03-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2eb03-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="2eb03-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="2eb03-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb03-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2eb03-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2eb03-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2eb03-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2eb03-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb03-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2eb03-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2eb03-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2eb03-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2eb03-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2eb03-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="2eb03-129">Para esta clase, la cadena es "./Vendor/MSFT/WindowsLicensing".</span><span class="sxs-lookup"><span data-stu-id="2eb03-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="2eb03-130">Estado</span><span class="sxs-lookup"><span data-stu-id="2eb03-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eb03-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2eb03-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2eb03-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2eb03-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2eb03-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb03-133">Requirements</span></span>



| <span data-ttu-id="2eb03-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb03-134">Requirement</span></span> | <span data-ttu-id="2eb03-135">Value</span><span class="sxs-lookup"><span data-stu-id="2eb03-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb03-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb03-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb03-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2eb03-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2eb03-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb03-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb03-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2eb03-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2eb03-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2eb03-140">Namespace</span></span><br/>                | <span data-ttu-id="2eb03-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2eb03-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2eb03-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2eb03-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eb03-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eb03-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eb03-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2eb03-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eb03-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eb03-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

