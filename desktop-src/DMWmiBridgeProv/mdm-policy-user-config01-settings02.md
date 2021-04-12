---
title: MDM_Policy_User_Config01_Settings02 (clase)
description: La \_ \_ clase Config01 de usuario de directiva de MDM \_ \_ Settings02 configura calendarios adicionales en la barra de tareas.
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- MDM_Policy_User_Config01_Settings02 (clase)
- MDM_Policy_User_Config01_Settings02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150347"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="6b186-105">\_Clase Settings02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="6b186-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="6b186-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6b186-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6b186-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6b186-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6b186-108">La \_ \_ clase Config01 de usuario de directiva de MDM \_ \_ Settings02 configura calendarios adicionales en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6b186-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="6b186-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6b186-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b186-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b186-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="6b186-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b186-111">Members</span></span>

<span data-ttu-id="6b186-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Settings02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b186-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="6b186-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b186-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b186-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b186-114">Properties</span></span>

<span data-ttu-id="6b186-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Settings02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b186-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6b186-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="6b186-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b186-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b186-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b186-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b186-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6b186-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6b186-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b186-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b186-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b186-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b186-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b186-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b186-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6b186-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6b186-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b186-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b186-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b186-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b186-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b186-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b186-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b186-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b186-127">Requirements</span></span>



| <span data-ttu-id="6b186-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b186-128">Requirement</span></span> | <span data-ttu-id="6b186-129">Value</span><span class="sxs-lookup"><span data-stu-id="6b186-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b186-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b186-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b186-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b186-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b186-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b186-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b186-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6b186-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6b186-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b186-134">Namespace</span></span><br/>                | <span data-ttu-id="6b186-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="6b186-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6b186-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6b186-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b186-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b186-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b186-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b186-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b186-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b186-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

