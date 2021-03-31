---
description: Las siguientes constantes forman el conjunto de comandos válidos de dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandos de dispositivo WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907999"
---
# <a name="wia-device-commands"></a><span data-ttu-id="29d46-103">Comandos de dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="29d46-103">WIA Device Commands</span></span>

<span data-ttu-id="29d46-104">Las siguientes constantes forman el conjunto de comandos válidos de dispositivo de hardware de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="29d46-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="29d46-105">Constante</span><span class="sxs-lookup"><span data-stu-id="29d46-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="29d46-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="29d46-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="29d46-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-108">Hace que el minicontrolador del dispositivo sincronice los elementos almacenados en caché con el dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="29d46-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="29d46-109">Si el dispositivo admite el método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , la emisión de este comando hace que el minicontrolador descarte los resultados del análisis y restablezca el estado inicial del elemento.</span><span class="sxs-lookup"><span data-stu-id="29d46-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="29d46-110">Todos los controladores deben ser compatibles con este comando.</span><span class="sxs-lookup"><span data-stu-id="29d46-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="29d46-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-112">Hace que un dispositivo WIA adquiera una imagen.</span><span class="sxs-lookup"><span data-stu-id="29d46-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="29d46-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-114">Indica al dispositivo que elimine todos los elementos que se pueden eliminar del árbol de objetos <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> que representan el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29d46-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="29d46-115">La eliminación de elementos se evita estableciendo las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="29d46-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="29d46-116">Para obtener más información, vea <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> y <a href="-wia-property-attributes.md">atributos de propiedad</a>.</span><span class="sxs-lookup"><span data-stu-id="29d46-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="29d46-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-118">Se utiliza para los escáneres de documentos.</span><span class="sxs-lookup"><span data-stu-id="29d46-118">Used for document scanners.</span></span> <span data-ttu-id="29d46-119">Hace que el analizador cargue la siguiente página en su controlador de documentos.</span><span class="sxs-lookup"><span data-stu-id="29d46-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="29d46-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-121">Se utiliza para los escáneres de documentos.</span><span class="sxs-lookup"><span data-stu-id="29d46-121">Used for document scanners.</span></span> <span data-ttu-id="29d46-122">Indica al dispositivo que descargue todas las páginas restantes en su controlador de documentos.</span><span class="sxs-lookup"><span data-stu-id="29d46-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="29d46-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-124">Se usa para los escáneres de documentos que tienen un alimentador de páginas.</span><span class="sxs-lookup"><span data-stu-id="29d46-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="29d46-125">Indica al dispositivo que inicie el motor del alimentador.</span><span class="sxs-lookup"><span data-stu-id="29d46-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="29d46-126">Esta característica está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29d46-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29d46-127">El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> o se establece en WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="29d46-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="29d46-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-129">Se usa para los escáneres de documentos que tienen un alimentador de páginas.</span><span class="sxs-lookup"><span data-stu-id="29d46-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="29d46-130">Indica al dispositivo que detenga el motor del alimentador.</span><span class="sxs-lookup"><span data-stu-id="29d46-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="29d46-131">Esta característica está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29d46-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29d46-132">El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="29d46-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="29d46-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="29d46-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="29d46-134">Se usa para los escáneres de documentos que tienen un alimentador de páginas.</span><span class="sxs-lookup"><span data-stu-id="29d46-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="29d46-135">Indica al dispositivo que PAUSE el motor del alimentador.</span><span class="sxs-lookup"><span data-stu-id="29d46-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="29d46-136">Esta característica está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29d46-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29d46-137">El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="29d46-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="29d46-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d46-138">Requirements</span></span>



| <span data-ttu-id="29d46-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d46-139">Requirement</span></span> | <span data-ttu-id="29d46-140">Value</span><span class="sxs-lookup"><span data-stu-id="29d46-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29d46-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d46-141">Minimum supported client</span></span><br/> | <span data-ttu-id="29d46-142">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="29d46-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="29d46-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d46-143">Minimum supported server</span></span><br/> | <span data-ttu-id="29d46-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="29d46-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="29d46-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29d46-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d46-146"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d46-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
