---
description: La propiedad SourceListInfo del objeto patch obtiene y establece las propiedades de información de origen de una revisión. Esta propiedad llama a MsiSourceListGetInfo o MsiSourceListSetInfo. Se trata de una propiedad de lectura o escritura.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch. SourceListInfo (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653430"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="62513-105">Patch. SourceListInfo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="62513-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="62513-106">La propiedad **SourceListInfo** del objeto [**patch**](patch-object.md) obtiene y establece las propiedades de información de origen de una revisión.</span><span class="sxs-lookup"><span data-stu-id="62513-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="62513-107">Esta propiedad llama a [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="62513-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="62513-108">Se trata de una propiedad de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="62513-108">This is a read or write property.</span></span>

<span data-ttu-id="62513-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="62513-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62513-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62513-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="62513-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="62513-111">Property value</span></span>

<span data-ttu-id="62513-112">Nombre de las propiedades de información de origen de una revisión que se va a consultar o establecer.</span><span class="sxs-lookup"><span data-stu-id="62513-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="62513-113">Para ver los valores posibles, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="62513-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="62513-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62513-114">Remarks</span></span>

<span data-ttu-id="62513-115">No se pueden establecer todas las propiedades que se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="62513-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="62513-116">El parámetro *szProperty* puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="62513-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="62513-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62513-117">Property</span></span>         | <span data-ttu-id="62513-118">¿Se puede establecer?</span><span class="sxs-lookup"><span data-stu-id="62513-118">Can set?</span></span> | <span data-ttu-id="62513-119">Significado</span><span class="sxs-lookup"><span data-stu-id="62513-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62513-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="62513-120">MediaPackagePath</span></span> | <span data-ttu-id="62513-121">Y</span><span class="sxs-lookup"><span data-stu-id="62513-121">Y</span></span>        | <span data-ttu-id="62513-122">Ruta de acceso relativa a la raíz de los medios de instalación.</span><span class="sxs-lookup"><span data-stu-id="62513-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="62513-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="62513-123">DiskPrompt</span></span>       | <span data-ttu-id="62513-124">Y</span><span class="sxs-lookup"><span data-stu-id="62513-124">Y</span></span>        | <span data-ttu-id="62513-125">La plantilla de mensaje que se usa al solicitar al usuario el disco de instalación.</span><span class="sxs-lookup"><span data-stu-id="62513-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="62513-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="62513-126">LastUsedSource</span></span>   | <span data-ttu-id="62513-127">Y</span><span class="sxs-lookup"><span data-stu-id="62513-127">Y</span></span>        | <span data-ttu-id="62513-128">Ubicación de origen utilizada más recientemente para la revisión.</span><span class="sxs-lookup"><span data-stu-id="62513-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="62513-129">Al establecer esta propiedad, Prefije la ubicación de origen con "n;" para un origen de red o "u;" para el tipo de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="62513-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="62513-130">Por ejemplo, use "n; \\ \\ grietas Scratch \\ \\ "o" u; https://microsoft.com/Patches/Office/SP1 ".</span><span class="sxs-lookup"><span data-stu-id="62513-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="62513-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="62513-131">LastUsedType</span></span>     | <span data-ttu-id="62513-132">N</span><span class="sxs-lookup"><span data-stu-id="62513-132">N</span></span>        | <span data-ttu-id="62513-133">"n" si el origen que se usa por última vez es una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="62513-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="62513-134">"u" si el último origen utilizado era una ubicación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="62513-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="62513-135">"m" si el último origen utilizado era un medio.</span><span class="sxs-lookup"><span data-stu-id="62513-135">"m" if the last used source was media.</span></span> <span data-ttu-id="62513-136">Cadena vacía ("") si no hay ningún origen usado por última vez.</span><span class="sxs-lookup"><span data-stu-id="62513-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="62513-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="62513-137">PackageName</span></span>      | <span data-ttu-id="62513-138">Y</span><span class="sxs-lookup"><span data-stu-id="62513-138">Y</span></span>        | <span data-ttu-id="62513-139">Nombre del paquete de Windows Installer o paquete de revisión en el origen.</span><span class="sxs-lookup"><span data-stu-id="62513-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="62513-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62513-140">Requirements</span></span>



| <span data-ttu-id="62513-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="62513-141">Requirement</span></span> | <span data-ttu-id="62513-142">Value</span><span class="sxs-lookup"><span data-stu-id="62513-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62513-143">Versión</span><span class="sxs-lookup"><span data-stu-id="62513-143">Version</span></span><br/> | <span data-ttu-id="62513-144">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62513-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62513-145">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62513-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62513-146">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="62513-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="62513-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62513-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="62513-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62513-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="62513-149">IID</span><span class="sxs-lookup"><span data-stu-id="62513-149">IID</span></span><br/>     | <span data-ttu-id="62513-150">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="62513-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="62513-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="62513-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62513-152">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="62513-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="62513-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="62513-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="62513-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="62513-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="62513-155">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="62513-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




