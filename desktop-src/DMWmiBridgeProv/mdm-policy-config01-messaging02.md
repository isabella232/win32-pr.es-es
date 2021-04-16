---
title: MDM_Policy_Config01_Messaging02 (clase)
description: La \_ clase Config01 de Messaging02 de directivas MDM \_ habilita la copia de \_ seguridad y restauración de mensajes de texto en todas partes. Esta directiva permite a una organización deshabilitar estas características para evitar que se almacene en servidores fuera de su control.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- MDM_Policy_Config01_Messaging02 (clase)
- MDM_Policy_Config01_Messaging02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534120"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="b19c0-106">\_ \_ Clase Messaging02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="b19c0-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="b19c0-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b19c0-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b19c0-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b19c0-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b19c0-109">La \_ clase Config01 de Messaging02 de directivas MDM \_ habilita la copia de \_ seguridad y restauración de mensajes de texto en todas partes.</span><span class="sxs-lookup"><span data-stu-id="b19c0-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="b19c0-110">Esta directiva permite a una organización deshabilitar estas características para evitar que se almacene en servidores fuera de su control.</span><span class="sxs-lookup"><span data-stu-id="b19c0-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="b19c0-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b19c0-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19c0-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b19c0-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="b19c0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b19c0-113">Members</span></span>

<span data-ttu-id="b19c0-114">La clase Config01 de la **\_ Directiva MDM \_ \_ Messaging02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b19c0-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="b19c0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b19c0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b19c0-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b19c0-116">Properties</span></span>

<span data-ttu-id="b19c0-117">La **clase \_ \_ Config01 de \_ Messaging02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b19c0-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b19c0-118">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="b19c0-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b19c0-119">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b19c0-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b19c0-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b19c0-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b19c0-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b19c0-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b19c0-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b19c0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b19c0-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b19c0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b19c0-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b19c0-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b19c0-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b19c0-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b19c0-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b19c0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b19c0-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b19c0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b19c0-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b19c0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b19c0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b19c0-129">Requirements</span></span>



| <span data-ttu-id="b19c0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b19c0-130">Requirement</span></span> | <span data-ttu-id="b19c0-131">Value</span><span class="sxs-lookup"><span data-stu-id="b19c0-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b19c0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b19c0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b19c0-133">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b19c0-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b19c0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b19c0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b19c0-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b19c0-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b19c0-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b19c0-136">Namespace</span></span><br/>                | <span data-ttu-id="b19c0-137">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b19c0-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b19c0-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b19c0-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b19c0-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b19c0-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b19c0-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b19c0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b19c0-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b19c0-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

