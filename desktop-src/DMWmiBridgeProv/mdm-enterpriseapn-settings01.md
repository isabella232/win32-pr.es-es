---
title: MDM_EnterpriseAPN_Settings01 (clase)
description: '\_ \_ La empresa usa la clase Settings01 ENTERPRISEAPN de MDM para cambiar la configuración global de APN.'
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- MDM_EnterpriseAPN_Settings01 (clase)
- MDM_EnterpriseAPN_Settings01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150723"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="2d8e0-105">\_Clase Settings01 EnterpriseAPN de MDM \_</span><span class="sxs-lookup"><span data-stu-id="2d8e0-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="2d8e0-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2d8e0-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2d8e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2d8e0-108">La empresa usa la clase **\_ \_ Settings01 EnterpriseAPN de MDM** para cambiar la configuración global de APN.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="2d8e0-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8e0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d8e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="2d8e0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d8e0-111">Members</span></span>

<span data-ttu-id="2d8e0-112">La clase de **\_ \_ Settings01 EnterpriseAPN de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d8e0-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="2d8e0-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d8e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d8e0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d8e0-114">Properties</span></span>

<span data-ttu-id="2d8e0-115">La clase de **\_ \_ Settings01 EnterpriseAPN de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2d8e0-116">AllowUserControl</span><span class="sxs-lookup"><span data-stu-id="2d8e0-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d8e0-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2d8e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d8e0-119">HideView</span><span class="sxs-lookup"><span data-stu-id="2d8e0-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d8e0-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2d8e0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d8e0-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d8e0-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d8e0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d8e0-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2d8e0-126">Nodo que contiene la configuración global de APN.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="2d8e0-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d8e0-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2d8e0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d8e0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d8e0-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d8e0-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2d8e0-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2d8e0-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2d8e0-132">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseAPN/Settings".</span><span class="sxs-lookup"><span data-stu-id="2d8e0-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d8e0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d8e0-133">Requirements</span></span>



| <span data-ttu-id="2d8e0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8e0-134">Requirement</span></span> | <span data-ttu-id="2d8e0-135">Value</span><span class="sxs-lookup"><span data-stu-id="2d8e0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8e0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d8e0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8e0-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d8e0-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d8e0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d8e0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8e0-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2d8e0-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2d8e0-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d8e0-140">Namespace</span></span><br/>                | <span data-ttu-id="2d8e0-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2d8e0-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2d8e0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2d8e0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d8e0-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d8e0-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d8e0-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d8e0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d8e0-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d8e0-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

