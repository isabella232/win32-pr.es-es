---
title: MDM_Firewall_Action04 (clase)
description: La \_ clase Action04 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- MDM_Firewall_Action04 (clase)
- MDM_Firewall_Action04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489946"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="ce685-105">\_Clase Action04 de Firewall de MDM \_</span><span class="sxs-lookup"><span data-stu-id="ce685-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="ce685-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ce685-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce685-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ce685-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce685-108">La \_ clase Action04 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="ce685-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="ce685-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ce685-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce685-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce685-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="ce685-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce685-111">Members</span></span>

<span data-ttu-id="ce685-112">La **clase \_ \_ Action04 de Firewall de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ce685-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="ce685-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce685-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce685-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce685-114">Properties</span></span>

<span data-ttu-id="ce685-115">La **clase \_ \_ Action04 de Firewall de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce685-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce685-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce685-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce685-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ce685-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce685-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ce685-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce685-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce685-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce685-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ce685-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce685-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ce685-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce685-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ce685-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce685-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce685-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce685-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ce685-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce685-125">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ce685-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce685-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ce685-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce685-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce685-127">Requirements</span></span>



| <span data-ttu-id="ce685-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce685-128">Requirement</span></span> | <span data-ttu-id="ce685-129">Value</span><span class="sxs-lookup"><span data-stu-id="ce685-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce685-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce685-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ce685-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce685-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce685-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce685-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ce685-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce685-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ce685-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce685-134">Namespace</span></span><br/>                | <span data-ttu-id="ce685-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ce685-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="ce685-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ce685-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce685-137"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce685-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce685-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce685-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce685-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce685-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

