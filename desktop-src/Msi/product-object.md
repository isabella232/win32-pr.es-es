---
description: El objeto Product representa una instancia única de un producto anunciado, instalado o desconocido. Se puede crear una instancia del objeto con la propiedad Product como &\# 0034; WindowsInstaller. Installer. Product (ProductCode, UserSid, context) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Objeto Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653484"
---
# <a name="product-object"></a><span data-ttu-id="dae7a-103">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="dae7a-103">Product object</span></span>

<span data-ttu-id="dae7a-104">El objeto **Product** representa una instancia única de un producto anunciado, instalado o desconocido.</span><span class="sxs-lookup"><span data-stu-id="dae7a-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="dae7a-105">Se puede crear una instancia del objeto con la propiedad **Product** como "WindowsInstaller. Installer. Product (*ProductCode*, *UserSid*, *Context*)".</span><span class="sxs-lookup"><span data-stu-id="dae7a-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="dae7a-106">*UserSid* debe ser null para el contexto por máquina.</span><span class="sxs-lookup"><span data-stu-id="dae7a-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="dae7a-107">*UserSid* puede ser null para el usuario actual especificado, cuando el contexto no es por equipo.</span><span class="sxs-lookup"><span data-stu-id="dae7a-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="dae7a-108">Los parámetros *ProductCode* y *Context* son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="dae7a-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="dae7a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dae7a-109">Members</span></span>

<span data-ttu-id="dae7a-110">El objeto **Product** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dae7a-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="dae7a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae7a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dae7a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dae7a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dae7a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae7a-113">Methods</span></span>

<span data-ttu-id="dae7a-114">El objeto **Product** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dae7a-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="dae7a-115">Método</span><span class="sxs-lookup"><span data-stu-id="dae7a-115">Method</span></span>                                                                 | <span data-ttu-id="dae7a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dae7a-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dae7a-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="dae7a-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="dae7a-118">Agregue un disco al conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="dae7a-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="dae7a-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="dae7a-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="dae7a-120">Agregue una red o un origen de URL a la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dae7a-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="dae7a-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="dae7a-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="dae7a-122">Borra la lista de origen completa del tipo de orígenes especificado.</span><span class="sxs-lookup"><span data-stu-id="dae7a-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="dae7a-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="dae7a-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="dae7a-124">Quitar un disco del conjunto de discos registrados de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dae7a-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="dae7a-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="dae7a-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="dae7a-126">Quite una red o un origen de la dirección URL de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dae7a-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="dae7a-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="dae7a-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="dae7a-128">Borra el origen usado por última vez.</span><span class="sxs-lookup"><span data-stu-id="dae7a-128">Clears the last used source.</span></span> <span data-ttu-id="dae7a-129">Esto fuerza la resolución de una lista de origen la próxima vez que se requiera el origen.</span><span class="sxs-lookup"><span data-stu-id="dae7a-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dae7a-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dae7a-130">Properties</span></span>

<span data-ttu-id="dae7a-131">El objeto **Product** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dae7a-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="dae7a-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dae7a-132">Property</span></span>                                                      | <span data-ttu-id="dae7a-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="dae7a-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dae7a-134">**ComponentState**</span><span class="sxs-lookup"><span data-stu-id="dae7a-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="dae7a-135">El estado de un componente especificado para esta instancia de producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="dae7a-136">**Context**</span><span class="sxs-lookup"><span data-stu-id="dae7a-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="dae7a-137">Contexto de esta instancia de producto como un valor de MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="dae7a-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="dae7a-138">**FeatureState**</span><span class="sxs-lookup"><span data-stu-id="dae7a-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="dae7a-139">El estado de una característica especificada para esta instancia de producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="dae7a-140">**InstallProperty**</span><span class="sxs-lookup"><span data-stu-id="dae7a-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="dae7a-141">Valor de una propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="dae7a-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="dae7a-142">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="dae7a-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="dae7a-143">Enumera todos los discos multimedia para esta instancia de producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="dae7a-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="dae7a-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="dae7a-145">Devuelve el código de producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="dae7a-146">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="dae7a-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="dae7a-147">Obtiene y establece las propiedades de información de origen.</span><span class="sxs-lookup"><span data-stu-id="dae7a-147">Get and set the source information properties.</span></span> <span data-ttu-id="dae7a-148">Se trata de una propiedad de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="dae7a-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="dae7a-149">**Orígenes**</span><span class="sxs-lookup"><span data-stu-id="dae7a-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="dae7a-150">Enumera todos los orígenes de esta instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="dae7a-151">**State**</span><span class="sxs-lookup"><span data-stu-id="dae7a-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="dae7a-152">Estado de instalación del producto.</span><span class="sxs-lookup"><span data-stu-id="dae7a-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="dae7a-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="dae7a-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="dae7a-154">Devuelve el SID de usuario, en el que esta instancia de producto está disponible.</span><span class="sxs-lookup"><span data-stu-id="dae7a-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="dae7a-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae7a-155">Requirements</span></span>



| <span data-ttu-id="dae7a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae7a-156">Requirement</span></span> | <span data-ttu-id="dae7a-157">Value</span><span class="sxs-lookup"><span data-stu-id="dae7a-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae7a-158">Versión</span><span class="sxs-lookup"><span data-stu-id="dae7a-158">Version</span></span><br/> | <span data-ttu-id="dae7a-159">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dae7a-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dae7a-160">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dae7a-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dae7a-161">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dae7a-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="dae7a-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dae7a-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="dae7a-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae7a-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="dae7a-164">IID</span><span class="sxs-lookup"><span data-stu-id="dae7a-164">IID</span></span><br/>     | <span data-ttu-id="dae7a-165">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dae7a-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="dae7a-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="dae7a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae7a-167">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dae7a-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




