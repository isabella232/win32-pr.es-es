---
description: Estas marcas especifican el comportamiento del localizador de medios.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Marcas de validación de nombre de archivo (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679559"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="bc827-103">Marcas de validación de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="bc827-103">File Name Validation Flags</span></span>

<span data-ttu-id="bc827-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="bc827-104">\[Deprecated.</span></span> <span data-ttu-id="bc827-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc827-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="bc827-106">Estas marcas especifican el comportamiento del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="bc827-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="bc827-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="bc827-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="bc827-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc827-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="bc827-109"><dt>**SFN \_ VALIDATEF \_ comprobar**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="bc827-110">Compruebe la validez de los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="bc827-110">Check the validity of file names.</span></span> <span data-ttu-id="bc827-111">Debe establecer esta marca para validar los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="bc827-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="bc827-112">En caso contrario, los demás marcadores no tienen ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="bc827-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="bc827-113"><dt>**SFN \_ VALIDATEF \_ emergente**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="bc827-114">Si no se encuentra un archivo, muestra un cuadro de diálogo Abrir archivo para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="bc827-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="bc827-115"><dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="bc827-116">Si se encuentra un archivo que falta, muestre brevemente un cuadro de mensaje con el nombre y la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="bc827-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="bc827-117">Esta marca es principalmente útil para fines de prueba; es probable que el cuadro de mensaje no sea adecuado para un producto comercial.</span><span class="sxs-lookup"><span data-stu-id="bc827-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="bc827-118"><dt>**SFN \_ VALIDATEF \_ reemplazar**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="bc827-119">Si se encuentra un archivo que falta, actualice el nombre del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="bc827-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="bc827-120">(Solo es válido en el método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).</span><span class="sxs-lookup"><span data-stu-id="bc827-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="bc827-121"><dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="bc827-122">Use siempre un archivo local, incluso si existe una versión del archivo en la red.</span><span class="sxs-lookup"><span data-stu-id="bc827-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="bc827-123"><dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="bc827-124">No busque archivos que faltan.</span><span class="sxs-lookup"><span data-stu-id="bc827-124">Do not search for missing files.</span></span> <span data-ttu-id="bc827-125">Los nombres de archivo siguen validados si se establece la \_ marca de comprobación de VALIDATEF de SFN \_ .</span><span class="sxs-lookup"><span data-stu-id="bc827-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="bc827-126"><dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="bc827-127">Omitir objetos de origen silenciados.</span><span class="sxs-lookup"><span data-stu-id="bc827-127">Ignore muted source objects.</span></span> <span data-ttu-id="bc827-128">(Solo es válido en el método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).</span><span class="sxs-lookup"><span data-stu-id="bc827-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="bc827-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc827-129">Requirements</span></span>



| <span data-ttu-id="bc827-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc827-130">Requirement</span></span> | <span data-ttu-id="bc827-131">Value</span><span class="sxs-lookup"><span data-stu-id="bc827-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc827-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc827-132">Header</span></span><br/> | <dl> <span data-ttu-id="bc827-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc827-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc827-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc827-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc827-135">**IMediaLocator::FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="bc827-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="bc827-136">**IRenderEngine::SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="bc827-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




