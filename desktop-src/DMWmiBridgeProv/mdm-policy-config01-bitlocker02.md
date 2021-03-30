---
title: MDM_Policy_Config01_BitLocker02 (clase)
description: La \_ clase Config01 de Bitlocker02 de directivas MDM \_ \_ representa las directivas de BitLocker disponibles.
ms.assetid: 885df93f-41f5-4cf7-8bce-9b253b190e17
keywords:
- MDM_Policy_Config01_BitLocker02 (clase)
- MDM_Policy_Config01_BitLocker02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02.InstanceID
- MDM_Policy_Config01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 005c16365dfc227aff4c854e77b2a733a3c4ac70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079181"
---
# <a name="mdm_policy_config01_bitlocker02-class"></a><span data-ttu-id="88597-105">\_ \_ Clase BitLocker02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="88597-105">MDM\_Policy\_Config01\_BitLocker02 class</span></span>

<span data-ttu-id="88597-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="88597-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="88597-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="88597-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="88597-108">La **clase \_ \_ Config01 de \_ Bitlocker02 de directivas MDM** representa las directivas de BitLocker disponibles.</span><span class="sxs-lookup"><span data-stu-id="88597-108">The **MDM\_Policy\_Config01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="88597-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="88597-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88597-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88597-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="88597-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="88597-111">Members</span></span>

<span data-ttu-id="88597-112">La clase Config01 de la **\_ Directiva MDM \_ \_ BitLocker02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88597-112">The **MDM\_Policy\_Config01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="88597-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88597-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88597-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88597-114">Properties</span></span>

<span data-ttu-id="88597-115">La **clase \_ \_ Config01 de \_ BitLocker02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="88597-115">The **MDM\_Policy\_Config01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="88597-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="88597-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88597-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="88597-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="88597-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="88597-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88597-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="88597-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88597-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88597-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88597-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88597-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88597-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88597-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88597-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="88597-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="88597-124">Para esta clase, la cadena es "BitLocker"</span><span class="sxs-lookup"><span data-stu-id="88597-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="88597-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="88597-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88597-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="88597-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88597-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88597-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88597-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88597-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88597-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="88597-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="88597-130">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="88597-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88597-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88597-131">Requirements</span></span>



| <span data-ttu-id="88597-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="88597-132">Requirement</span></span> | <span data-ttu-id="88597-133">Value</span><span class="sxs-lookup"><span data-stu-id="88597-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88597-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88597-134">Minimum supported client</span></span><br/> | <span data-ttu-id="88597-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="88597-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88597-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88597-136">Minimum supported server</span></span><br/> | <span data-ttu-id="88597-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88597-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="88597-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88597-138">Namespace</span></span><br/>                | <span data-ttu-id="88597-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="88597-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="88597-140">MOF</span><span class="sxs-lookup"><span data-stu-id="88597-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88597-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88597-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="88597-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88597-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88597-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88597-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88597-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="88597-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88597-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="88597-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

