---
description: La interfaz IDxtJpeg establece las propiedades en la transición de borrado de SMPTE. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de borrado de SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaz IDxtJpeg (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679425"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="fe690-103">Interfaz IDxtJpeg</span><span class="sxs-lookup"><span data-stu-id="fe690-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="fe690-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fe690-104">\[Deprecated.</span></span> <span data-ttu-id="fe690-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe690-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe690-106">La `IDxtJpeg` interfaz establece las propiedades en la transición de [borrado de SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="fe690-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="fe690-107">Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de borrado de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="fe690-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="fe690-108">Las aplicaciones DES no necesitan usar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="fe690-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="fe690-109">Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="fe690-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="fe690-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe690-110">Members</span></span>

<span data-ttu-id="fe690-111">La interfaz **IDxtJpeg** hereda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="fe690-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="fe690-112">**IDxtJpeg** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fe690-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="fe690-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe690-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe690-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe690-114">Methods</span></span>

<span data-ttu-id="fe690-115">La interfaz **IDxtJpeg** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fe690-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="fe690-116">Método</span><span class="sxs-lookup"><span data-stu-id="fe690-116">Method</span></span>                                                     | <span data-ttu-id="fe690-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe690-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe690-118">**ApplyChanges (**</span><span class="sxs-lookup"><span data-stu-id="fe690-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="fe690-119">Aplica las propiedades que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="fe690-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="fe690-120">**obtener \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="fe690-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="fe690-121">Recupera el color del borde alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="fe690-122">**obtener \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="fe690-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="fe690-123">Recupera el ancho de la región borrosa alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="fe690-124">**obtener \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="fe690-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="fe690-125">Recupera el ancho del borde sólido a lo largo de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="fe690-126">**obtener \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="fe690-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="fe690-127">Recupera el nombre de un archivo JPEG que se usará como máscara de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="fe690-128">**obtener \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="fe690-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="fe690-129">Recupera el código de borrado de SMPTE de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="fe690-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="fe690-130">**obtener \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="fe690-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="fe690-131">Recupera el desplazamiento horizontal del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="fe690-132">**obtener \_ desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="fe690-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="fe690-133">Recupera el desplazamiento vertical del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="fe690-134">**obtener \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="fe690-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="fe690-135">Recupera el número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="fe690-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="fe690-136">**obtención de \_ replicación**</span><span class="sxs-lookup"><span data-stu-id="fe690-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="fe690-137">Recupera el número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fe690-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="fe690-138">**obtener \_ scaleX**</span><span class="sxs-lookup"><span data-stu-id="fe690-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="fe690-139">Recupera la cantidad por la que se ajusta horizontalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="fe690-140">**obtener \_ escalado**</span><span class="sxs-lookup"><span data-stu-id="fe690-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="fe690-141">Recupera la cantidad por la que se ajusta verticalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="fe690-142">**LoadDefSettings**</span><span class="sxs-lookup"><span data-stu-id="fe690-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="fe690-143">Restaura la configuración predeterminada de la transición de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="fe690-144">**poner \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="fe690-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="fe690-145">Especifica el color del borde alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="fe690-146">**Put \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="fe690-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="fe690-147">Especifica el ancho de la región borrosa alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="fe690-148">**poner \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="fe690-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="fe690-149">Especifica el ancho del borde sólido a lo largo de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="fe690-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="fe690-150">**Put \_ MaskName**</span><span class="sxs-lookup"><span data-stu-id="fe690-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="fe690-151">Especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="fe690-152">**Put \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="fe690-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="fe690-153">Especifica el código de borrado de SMPTE de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="fe690-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="fe690-154">**Put \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="fe690-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="fe690-155">Especifica el desplazamiento horizontal del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="fe690-156">**colocar \_ desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="fe690-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="fe690-157">Especifica el desplazamiento vertical del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="fe690-158">**Put \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="fe690-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="fe690-159">Especifica el número de veces que el patrón de barrido se replica horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="fe690-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="fe690-160">**poner en \_ replicación**</span><span class="sxs-lookup"><span data-stu-id="fe690-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="fe690-161">Especifica el número de veces que el patrón de barrido se replica verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fe690-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="fe690-162">**poner \_ scaleX**</span><span class="sxs-lookup"><span data-stu-id="fe690-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="fe690-163">Especifica la cantidad por la que se ajusta horizontalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="fe690-164">**colocar \_ escalado**</span><span class="sxs-lookup"><span data-stu-id="fe690-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="fe690-165">Especifica la cantidad por la que se ajusta verticalmente el borrado.</span><span class="sxs-lookup"><span data-stu-id="fe690-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="fe690-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe690-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe690-167">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fe690-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe690-168">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fe690-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe690-169">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fe690-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe690-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe690-170">Requirements</span></span>



| <span data-ttu-id="fe690-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe690-171">Requirement</span></span> | <span data-ttu-id="fe690-172">Value</span><span class="sxs-lookup"><span data-stu-id="fe690-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe690-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe690-173">Header</span></span><br/>  | <dl> <span data-ttu-id="fe690-174"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe690-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe690-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe690-175">Library</span></span><br/> | <dl> <span data-ttu-id="fe690-176"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe690-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




