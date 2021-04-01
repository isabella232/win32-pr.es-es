---
title: MDM_SecureAssessment (clase)
description: La SecureAssessmentclass de MDM \_ se usa para proporcionar información de configuración para el explorador de evaluación segura.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- MDM_SecureAssessment (clase)
- MDM_SecureAssessment clase, descrita
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995961"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="929f7-105">\_Clase SecureAssessment de MDM</span><span class="sxs-lookup"><span data-stu-id="929f7-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="929f7-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="929f7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="929f7-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="929f7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="929f7-108">La **clase \_ SecureAssessment de MDM** se usa para proporcionar información de configuración para el explorador de evaluación segura.</span><span class="sxs-lookup"><span data-stu-id="929f7-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="929f7-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="929f7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="929f7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="929f7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="929f7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="929f7-111">Members</span></span>

<span data-ttu-id="929f7-112">La **clase \_ SecureAssessment de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="929f7-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="929f7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="929f7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="929f7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="929f7-114">Properties</span></span>

<span data-ttu-id="929f7-115">La **clase \_ SecureAssessment de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="929f7-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="929f7-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="929f7-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="929f7-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="929f7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="929f7-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="929f7-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="929f7-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="929f7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="929f7-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="929f7-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="929f7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="929f7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929f7-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="929f7-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="929f7-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="929f7-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="929f7-127">Para esta clase, la cadena es "SecureAssessment".</span><span class="sxs-lookup"><span data-stu-id="929f7-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="929f7-128">LaunchURI</span><span class="sxs-lookup"><span data-stu-id="929f7-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="929f7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="929f7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="929f7-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="929f7-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="929f7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="929f7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="929f7-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="929f7-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="929f7-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="929f7-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="929f7-136">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="929f7-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="929f7-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="929f7-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="929f7-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="929f7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="929f7-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="929f7-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="929f7-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="929f7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="929f7-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="929f7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="929f7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="929f7-143">Requirements</span></span>



| <span data-ttu-id="929f7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="929f7-144">Requirement</span></span> | <span data-ttu-id="929f7-145">Value</span><span class="sxs-lookup"><span data-stu-id="929f7-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="929f7-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="929f7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="929f7-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="929f7-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="929f7-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="929f7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="929f7-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="929f7-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="929f7-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="929f7-150">Namespace</span></span><br/>                | <span data-ttu-id="929f7-151">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="929f7-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="929f7-152">MOF</span><span class="sxs-lookup"><span data-stu-id="929f7-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="929f7-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="929f7-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="929f7-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="929f7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="929f7-155"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="929f7-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

