---
title: MDM_Policy_User_Result01_Printers02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Printers02 representa las directivas de impresora disponibles.
ms.assetid: c9555ba3-589c-4b9f-8fad-86fcda031555
keywords:
- MDM_Policy_User_Result01_Printers02 (clase)
- MDM_Policy_User_Result01_Printers02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Printers02
- MDM_Policy_User_Result01_Printers02.InstanceID
- MDM_Policy_User_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a93e2547fbdd8d2d8883d187fca758d5d0b592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801214"
---
# <a name="mdm_policy_user_result01_printers02-class"></a><span data-ttu-id="9a71e-105">\_Clase Printers02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="9a71e-105">MDM\_Policy\_User\_Result01\_Printers02 class</span></span>

<span data-ttu-id="9a71e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9a71e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9a71e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9a71e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9a71e-108">La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Printers02 representa las directivas de impresora disponibles.</span><span class="sxs-lookup"><span data-stu-id="9a71e-108">The MDM\_Policy\_User\_Result01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="9a71e-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9a71e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a71e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a71e-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="9a71e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a71e-111">Members</span></span>

<span data-ttu-id="9a71e-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Printers02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a71e-112">The **MDM\_Policy\_User\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="9a71e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a71e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a71e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a71e-114">Properties</span></span>

<span data-ttu-id="9a71e-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Printers02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a71e-115">The **MDM\_Policy\_User\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a71e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9a71e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a71e-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a71e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a71e-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a71e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a71e-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a71e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9a71e-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9a71e-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a71e-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a71e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a71e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a71e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a71e-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9a71e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9a71e-124">\_Usuario PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="9a71e-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a71e-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a71e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a71e-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a71e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a71e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a71e-127">Requirements</span></span>



| <span data-ttu-id="9a71e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a71e-128">Requirement</span></span> | <span data-ttu-id="9a71e-129">Value</span><span class="sxs-lookup"><span data-stu-id="9a71e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a71e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a71e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a71e-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a71e-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a71e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a71e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a71e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9a71e-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9a71e-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a71e-134">Namespace</span></span><br/>                | <span data-ttu-id="9a71e-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9a71e-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9a71e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9a71e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a71e-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a71e-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a71e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a71e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a71e-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a71e-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

