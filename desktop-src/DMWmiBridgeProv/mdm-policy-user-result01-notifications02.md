---
title: MDM_Policy_User_Result01_Notifications02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Notifications02 representa las directivas de notificación disponibles.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- MDM_Policy_User_Result01_Notifications02 (clase)
- MDM_Policy_User_Result01_Notifications02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c917e42ef568783b1c804ce17d52474a86359e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078912"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a><span data-ttu-id="7b511-105">\_Clase Notifications02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="7b511-105">MDM\_Policy\_User\_Result01\_Notifications02 class</span></span>

<span data-ttu-id="7b511-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7b511-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b511-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7b511-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b511-108">La **clase \_ Result01 de usuario de directiva de MDM \_ \_ \_ Notifications02** representa las directivas de notificación disponibles.</span><span class="sxs-lookup"><span data-stu-id="7b511-108">The **MDM\_Policy\_User\_Result01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="7b511-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7b511-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b511-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b511-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="7b511-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b511-111">Members</span></span>

<span data-ttu-id="7b511-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Notifications02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b511-112">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="7b511-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b511-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b511-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b511-114">Properties</span></span>

<span data-ttu-id="7b511-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Notifications02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7b511-115">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7b511-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="7b511-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b511-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b511-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b511-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7b511-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b511-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b511-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b511-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b511-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b511-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b511-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b511-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b511-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b511-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7b511-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="7b511-124">Para esta clase, la cadena es "notifications".</span><span class="sxs-lookup"><span data-stu-id="7b511-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="7b511-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7b511-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b511-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7b511-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b511-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7b511-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b511-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b511-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b511-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7b511-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="7b511-130">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="7b511-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b511-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b511-131">Requirements</span></span>



| <span data-ttu-id="7b511-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b511-132">Requirement</span></span> | <span data-ttu-id="7b511-133">Value</span><span class="sxs-lookup"><span data-stu-id="7b511-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b511-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b511-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b511-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b511-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7b511-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b511-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b511-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7b511-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="7b511-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b511-138">Namespace</span></span><br/>                | <span data-ttu-id="7b511-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7b511-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="7b511-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7b511-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b511-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b511-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="7b511-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b511-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b511-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b511-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

