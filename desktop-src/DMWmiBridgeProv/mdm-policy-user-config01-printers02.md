---
title: MDM_Policy_User_Config01_Printers02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Printers02 representa las directivas de impresora disponibles.
ms.assetid: 9faeaa04-92b4-43b0-be17-0f85f2eb493c
keywords:
- MDM_Policy_User_Config01_Printers02 (clase)
- MDM_Policy_User_Config01_Printers02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02.InstanceID
- MDM_Policy_User_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04be571473f05d93242c77d02052cf84c335caf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802395"
---
# <a name="mdm_policy_user_config01_printers02-class"></a><span data-ttu-id="effa0-105">\_Clase Printers02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="effa0-105">MDM\_Policy\_User\_Config01\_Printers02 class</span></span>

<span data-ttu-id="effa0-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="effa0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="effa0-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="effa0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="effa0-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Printers02 representa las directivas de impresora disponibles.</span><span class="sxs-lookup"><span data-stu-id="effa0-108">The MDM\_Policy\_User\_Config01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="effa0-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="effa0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="effa0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="effa0-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="effa0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="effa0-111">Members</span></span>

<span data-ttu-id="effa0-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Printers02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="effa0-112">The **MDM\_Policy\_User\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="effa0-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="effa0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="effa0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="effa0-114">Properties</span></span>

<span data-ttu-id="effa0-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Printers02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="effa0-115">The **MDM\_Policy\_User\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="effa0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="effa0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effa0-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="effa0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effa0-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="effa0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="effa0-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="effa0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="effa0-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="effa0-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effa0-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="effa0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effa0-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="effa0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="effa0-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="effa0-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="effa0-124">\_Usuario PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="effa0-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="effa0-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="effa0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effa0-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="effa0-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="effa0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effa0-127">Requirements</span></span>



| <span data-ttu-id="effa0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="effa0-128">Requirement</span></span> | <span data-ttu-id="effa0-129">Value</span><span class="sxs-lookup"><span data-stu-id="effa0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effa0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effa0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="effa0-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="effa0-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="effa0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effa0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="effa0-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="effa0-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="effa0-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="effa0-134">Namespace</span></span><br/>                | <span data-ttu-id="effa0-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="effa0-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="effa0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="effa0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="effa0-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="effa0-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="effa0-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="effa0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="effa0-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="effa0-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

