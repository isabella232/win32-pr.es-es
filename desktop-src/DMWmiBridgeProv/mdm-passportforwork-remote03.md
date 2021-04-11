---
title: MDM_PassportForWork_Remote03 (clase)
description: La \_ clase Remote03 de MDM PassportForWork \_ define la configuración de la Directiva remota de Windows Hello para empresas.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- MDM_PassportForWork_Remote03 (clase)
- MDM_PassportForWork_Remote03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079188"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="b92b2-105">\_Clase Remote03 PassportForWork de MDM \_</span><span class="sxs-lookup"><span data-stu-id="b92b2-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="b92b2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b92b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b92b2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b92b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b92b2-108">La **clase \_ \_ Remote03 de MDM PassportForWork** define la configuración de la Directiva remota de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="b92b2-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="b92b2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b92b2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b92b2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b92b2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="b92b2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b92b2-111">Members</span></span>

<span data-ttu-id="b92b2-112">La **clase \_ \_ Remote03 de MDM PassportForWork** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b92b2-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="b92b2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b92b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b92b2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b92b2-114">Properties</span></span>

<span data-ttu-id="b92b2-115">La **clase \_ \_ Remote03 de MDM PassportForWork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b92b2-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b92b2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b92b2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92b2-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b92b2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b92b2-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b92b2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b92b2-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b92b2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b92b2-120">Nodo interior para definir directivas de Windows Hello para empresas remotas.</span><span class="sxs-lookup"><span data-stu-id="b92b2-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="b92b2-121">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="b92b2-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="b92b2-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b92b2-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92b2-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b92b2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b92b2-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b92b2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b92b2-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b92b2-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b92b2-126">Nodo para definir la configuración de la Directiva de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="b92b2-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="b92b2-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="b92b2-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92b2-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b92b2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b92b2-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b92b2-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b92b2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92b2-130">Requirements</span></span>



| <span data-ttu-id="b92b2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92b2-131">Requirement</span></span> | <span data-ttu-id="b92b2-132">Value</span><span class="sxs-lookup"><span data-stu-id="b92b2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92b2-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b92b2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b92b2-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b92b2-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b92b2-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b92b2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b92b2-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b92b2-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b92b2-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b92b2-137">Namespace</span></span><br/>                | <span data-ttu-id="b92b2-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b92b2-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b92b2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b92b2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b92b2-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b92b2-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b92b2-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b92b2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b92b2-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b92b2-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b92b2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b92b2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92b2-144">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="b92b2-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

