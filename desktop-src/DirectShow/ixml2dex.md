---
description: La interfaz IXml2Dex guarda y carga los archivos de proyecto de servicios de edición de DirectShow (DES) en lenguaje de marcado extensible (XML). Esta interfaz también proporciona métodos para leer y escribir archivos de gráficos de DirectShow (. GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaz IXml2Dex (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690908"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="72c9c-104">Interfaz IXml2Dex</span><span class="sxs-lookup"><span data-stu-id="72c9c-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="72c9c-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="72c9c-105">\[Deprecated.</span></span> <span data-ttu-id="72c9c-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72c9c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72c9c-107">La `IXml2Dex` interfaz guarda y carga los archivos de proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) (DES) en lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="72c9c-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="72c9c-108">Esta interfaz también proporciona métodos para leer y escribir archivos de gráficos de DirectShow (. GRF).</span><span class="sxs-lookup"><span data-stu-id="72c9c-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="72c9c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="72c9c-109">Members</span></span>

<span data-ttu-id="72c9c-110">La interfaz **IXml2Dex** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="72c9c-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="72c9c-111">**IXml2Dex** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72c9c-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="72c9c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c9c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72c9c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c9c-113">Methods</span></span>

<span data-ttu-id="72c9c-114">La interfaz **IXml2Dex** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="72c9c-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="72c9c-115">Método</span><span class="sxs-lookup"><span data-stu-id="72c9c-115">Method</span></span>                                                      | <span data-ttu-id="72c9c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="72c9c-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="72c9c-117">**CopyXML**</span><span class="sxs-lookup"><span data-stu-id="72c9c-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="72c9c-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-119">**CreateGraphFromFile**</span><span class="sxs-lookup"><span data-stu-id="72c9c-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="72c9c-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-121">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="72c9c-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="72c9c-122">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-123">**PasteXML**</span><span class="sxs-lookup"><span data-stu-id="72c9c-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="72c9c-124">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-125">**PasteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="72c9c-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="72c9c-126">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-127">**ReadXML**</span><span class="sxs-lookup"><span data-stu-id="72c9c-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="72c9c-128">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-129">**ReadXMLFile**</span><span class="sxs-lookup"><span data-stu-id="72c9c-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="72c9c-130">Carga un archivo de proyecto XML.</span><span class="sxs-lookup"><span data-stu-id="72c9c-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="72c9c-131">**Reset**</span><span class="sxs-lookup"><span data-stu-id="72c9c-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="72c9c-132">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="72c9c-133">**WriteGrfFile**</span><span class="sxs-lookup"><span data-stu-id="72c9c-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="72c9c-134">Escribe un gráfico de filtro en un archivo en formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="72c9c-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="72c9c-135">**WriteXML**</span><span class="sxs-lookup"><span data-stu-id="72c9c-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="72c9c-136">Convierte una escala de tiempo en una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="72c9c-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="72c9c-137">**WriteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="72c9c-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="72c9c-138">Traduce una escala de tiempo a XML y escribe los datos XML en un archivo.</span><span class="sxs-lookup"><span data-stu-id="72c9c-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="72c9c-139">**WriteXMLPart**</span><span class="sxs-lookup"><span data-stu-id="72c9c-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="72c9c-140">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72c9c-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="72c9c-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72c9c-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72c9c-142">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="72c9c-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72c9c-143">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72c9c-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72c9c-144">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72c9c-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72c9c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c9c-145">Requirements</span></span>



| <span data-ttu-id="72c9c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c9c-146">Requirement</span></span> | <span data-ttu-id="72c9c-147">Value</span><span class="sxs-lookup"><span data-stu-id="72c9c-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72c9c-148">Versión</span><span class="sxs-lookup"><span data-stu-id="72c9c-148">Version</span></span><br/> | <span data-ttu-id="72c9c-149">Internet Explorer 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="72c9c-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="72c9c-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72c9c-150">Header</span></span><br/>  | <dl> <span data-ttu-id="72c9c-151"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c9c-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72c9c-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72c9c-152">Library</span></span><br/> | <dl> <span data-ttu-id="72c9c-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72c9c-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
