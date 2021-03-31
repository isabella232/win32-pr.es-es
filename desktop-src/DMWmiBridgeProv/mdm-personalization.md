---
title: MDM_Personalization (clase)
description: La \_ clase de personalización de MDM se usa para establecer la pantalla de bloqueo y las imágenes de fondo de escritorio. La configuración de estas directivas también impide que el usuario cambie la imagen.
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- MDM_Personalization (clase)
- MDM_Personalization clase, descrita
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996197"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="26ff0-106">\_Clase de personalización MDM</span><span class="sxs-lookup"><span data-stu-id="26ff0-106">MDM\_Personalization class</span></span>

<span data-ttu-id="26ff0-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="26ff0-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26ff0-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="26ff0-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26ff0-109">La \_ clase de personalización de MDM se usa para establecer la pantalla de bloqueo y las imágenes de fondo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="26ff0-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="26ff0-110">La configuración de estas directivas también impide que el usuario cambie la imagen.</span><span class="sxs-lookup"><span data-stu-id="26ff0-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="26ff0-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="26ff0-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ff0-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26ff0-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="26ff0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="26ff0-113">Members</span></span>

<span data-ttu-id="26ff0-114">La clase de **\_ Personalización de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="26ff0-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="26ff0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26ff0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26ff0-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26ff0-116">Properties</span></span>

<span data-ttu-id="26ff0-117">La clase de **\_ Personalización de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="26ff0-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="26ff0-118">DesktopImageStatus</span><span class="sxs-lookup"><span data-stu-id="26ff0-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-119">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26ff0-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26ff0-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26ff0-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="26ff0-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26ff0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26ff0-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26ff0-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26ff0-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26ff0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26ff0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26ff0-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26ff0-128">LockScreenImageStatus</span><span class="sxs-lookup"><span data-stu-id="26ff0-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26ff0-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26ff0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26ff0-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="26ff0-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26ff0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26ff0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26ff0-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26ff0-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ff0-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26ff0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26ff0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ff0-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26ff0-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26ff0-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26ff0-138">Requirements</span></span>



| <span data-ttu-id="26ff0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ff0-139">Requirement</span></span> | <span data-ttu-id="26ff0-140">Value</span><span class="sxs-lookup"><span data-stu-id="26ff0-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ff0-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ff0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="26ff0-142">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="26ff0-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26ff0-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ff0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="26ff0-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26ff0-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="26ff0-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26ff0-145">Namespace</span></span><br/>                | <span data-ttu-id="26ff0-146">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="26ff0-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="26ff0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="26ff0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26ff0-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26ff0-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="26ff0-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26ff0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ff0-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26ff0-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

