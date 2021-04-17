---
description: La propiedad SourceListInfo del objeto Product obtiene y establece las propiedades de información de origen de un producto. Esta propiedad llama a MsiSourceListGetInfo o MsiSourceListSetInfo. Se trata de una propiedad de lectura o escritura.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propiedad product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653810"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="95377-105">Propiedad product. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="95377-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="95377-106">La propiedad **SourceListInfo** del objeto [**Product**](product-object.md) obtiene y establece las propiedades de información de origen de un producto.</span><span class="sxs-lookup"><span data-stu-id="95377-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="95377-107">Esta propiedad llama a [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="95377-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="95377-108">Se trata de una propiedad de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="95377-108">This is a read or write property.</span></span>

<span data-ttu-id="95377-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="95377-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95377-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95377-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="95377-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="95377-111">Property value</span></span>

<span data-ttu-id="95377-112">Nombre de las propiedades de información de origen de un producto que se va a consultar o establecer.</span><span class="sxs-lookup"><span data-stu-id="95377-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="95377-113">Para ver los valores posibles, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="95377-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="95377-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95377-114">Remarks</span></span>

<span data-ttu-id="95377-115">No se pueden establecer todas las propiedades que se pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="95377-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="95377-116">El parámetro *szProperty* puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="95377-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="95377-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95377-117">Property</span></span>         | <span data-ttu-id="95377-118">¿Se puede establecer?</span><span class="sxs-lookup"><span data-stu-id="95377-118">Can set?</span></span> | <span data-ttu-id="95377-119">Significado</span><span class="sxs-lookup"><span data-stu-id="95377-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95377-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="95377-120">MediaPackagePath</span></span> | <span data-ttu-id="95377-121">Y</span><span class="sxs-lookup"><span data-stu-id="95377-121">Y</span></span>        | <span data-ttu-id="95377-122">Ruta de acceso relativa a la raíz de los medios de instalación.</span><span class="sxs-lookup"><span data-stu-id="95377-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="95377-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="95377-123">DiskPrompt</span></span>       | <span data-ttu-id="95377-124">Y</span><span class="sxs-lookup"><span data-stu-id="95377-124">Y</span></span>        | <span data-ttu-id="95377-125">La plantilla de mensaje que se usa al solicitar al usuario el disco de instalación.</span><span class="sxs-lookup"><span data-stu-id="95377-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="95377-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="95377-126">LastUsedSource</span></span>   | <span data-ttu-id="95377-127">Y</span><span class="sxs-lookup"><span data-stu-id="95377-127">Y</span></span>        | <span data-ttu-id="95377-128">La ubicación de origen utilizada más recientemente para el producto.</span><span class="sxs-lookup"><span data-stu-id="95377-128">The most recently used source location for the product.</span></span> <span data-ttu-id="95377-129">Al establecer esta propiedad, Prefije la ubicación de origen con "n;" para un origen de red o "u;" para el tipo de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="95377-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="95377-130">Por ejemplo, "n; \\ \\ Scratch \\ Scratch \\ "y" u; https://MyServer/MyFolder/MySource ".</span><span class="sxs-lookup"><span data-stu-id="95377-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="95377-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="95377-131">LastUsedType</span></span>     | <span data-ttu-id="95377-132">N</span><span class="sxs-lookup"><span data-stu-id="95377-132">N</span></span>        | <span data-ttu-id="95377-133">"n" si el origen que se usa por última vez es una ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="95377-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="95377-134">"u" si el último origen utilizado era una ubicación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="95377-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="95377-135">"m" si el último origen utilizado era un medio.</span><span class="sxs-lookup"><span data-stu-id="95377-135">"m" if the last used source was media.</span></span> <span data-ttu-id="95377-136">Cadena vacía ("") si no hay ningún origen usado por última vez.</span><span class="sxs-lookup"><span data-stu-id="95377-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="95377-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="95377-137">PackageName</span></span>      | <span data-ttu-id="95377-138">Y</span><span class="sxs-lookup"><span data-stu-id="95377-138">Y</span></span>        | <span data-ttu-id="95377-139">Nombre del paquete de Windows Installer o paquete de revisión en el origen.</span><span class="sxs-lookup"><span data-stu-id="95377-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="95377-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95377-140">Requirements</span></span>



| <span data-ttu-id="95377-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="95377-141">Requirement</span></span> | <span data-ttu-id="95377-142">Value</span><span class="sxs-lookup"><span data-stu-id="95377-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95377-143">Versión</span><span class="sxs-lookup"><span data-stu-id="95377-143">Version</span></span><br/> | <span data-ttu-id="95377-144">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95377-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="95377-145">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95377-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="95377-146">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="95377-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="95377-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95377-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="95377-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95377-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="95377-149">IID</span><span class="sxs-lookup"><span data-stu-id="95377-149">IID</span></span><br/>     | <span data-ttu-id="95377-150">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="95377-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="95377-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="95377-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95377-152">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="95377-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="95377-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="95377-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="95377-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="95377-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="95377-155">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="95377-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




