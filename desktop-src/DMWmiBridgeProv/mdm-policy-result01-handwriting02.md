---
title: MDM_Policy_Result01_Handwriting02 (clase)
description: La \_ \_ clase Result01 de la Directiva MDM \_ Handwriting02 representa el modo predeterminado del panel de escritura a mano.
ms.assetid: b21d0208-210d-476f-9269-f8d8a3307f17
keywords:
- MDM_Policy_Result01_Handwriting02 (clase)
- MDM_Policy_Result01_Handwriting02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Handwriting02
- MDM_Policy_Result01_Handwriting02.InstanceID
- MDM_Policy_Result01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636dcfbb0d3bceaf60697d2aaa6e7f158a052bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150399"
---
# <a name="mdm_policy_result01_handwriting02-class"></a><span data-ttu-id="ebc3b-105">\_ \_ Clase Handwriting02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="ebc3b-105">MDM\_Policy\_Result01\_Handwriting02 class</span></span>

<span data-ttu-id="ebc3b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ebc3b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ebc3b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ebc3b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ebc3b-108">La \_ \_ clase Result01 de la Directiva MDM \_ Handwriting02 representa el modo predeterminado del panel de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="ebc3b-108">The MDM\_Policy\_Result01\_Handwriting02 class represents the default mode for the handwriting panel.</span></span>

<span data-ttu-id="ebc3b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ebc3b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc3b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebc3b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="ebc3b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ebc3b-111">Members</span></span>

<span data-ttu-id="ebc3b-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Handwriting02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ebc3b-112">The **MDM\_Policy\_Result01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="ebc3b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebc3b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebc3b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebc3b-114">Properties</span></span>

<span data-ttu-id="ebc3b-115">La **clase \_ \_ Result01 de \_ Handwriting02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ebc3b-115">The **MDM\_Policy\_Result01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ebc3b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ebc3b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebc3b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ebc3b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebc3b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ebc3b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebc3b-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ebc3b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ebc3b-120">PanelDefaultModeDocked</span><span class="sxs-lookup"><span data-stu-id="ebc3b-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebc3b-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ebc3b-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ebc3b-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ebc3b-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ebc3b-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ebc3b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebc3b-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ebc3b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ebc3b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ebc3b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ebc3b-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ebc3b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebc3b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebc3b-127">Requirements</span></span>



| <span data-ttu-id="ebc3b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc3b-128">Requirement</span></span> | <span data-ttu-id="ebc3b-129">Value</span><span class="sxs-lookup"><span data-stu-id="ebc3b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc3b-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebc3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc3b-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebc3b-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebc3b-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebc3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc3b-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ebc3b-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ebc3b-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebc3b-134">Namespace</span></span><br/>                | <span data-ttu-id="ebc3b-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ebc3b-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ebc3b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ebc3b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebc3b-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebc3b-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebc3b-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebc3b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebc3b-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebc3b-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

