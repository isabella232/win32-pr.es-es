---
description: La interfaz IMediaLocator proporciona métodos para validar nombres de archivo en los servicios de edición de DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interfaz IMediaLocator (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679026"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="2d77a-103">Interfaz IMediaLocator</span><span class="sxs-lookup"><span data-stu-id="2d77a-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="2d77a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2d77a-104">\[Deprecated.</span></span> <span data-ttu-id="2d77a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d77a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d77a-106">La `IMediaLocator` interfaz proporciona métodos para validar nombres de archivo en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="2d77a-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="2d77a-107">Utilice esta interfaz para asegurarse de que un nombre de archivo y una ruta de acceso especificados corresponden a un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="2d77a-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="2d77a-108">Esta interfaz también proporciona una manera de buscar el archivo en otras ubicaciones y mostrar un cuadro de diálogo **abierto** para que el usuario pueda localizar el archivo.</span><span class="sxs-lookup"><span data-stu-id="2d77a-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="2d77a-109">El localizador multimedia implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2d77a-109">The media locator implements this interface.</span></span> <span data-ttu-id="2d77a-110">La escala de tiempo y el motor de representación también admiten la validación de nombres de archivo a través de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d77a-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="2d77a-111">[**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valida y actualiza los nombres de archivo en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2d77a-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="2d77a-112">[**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): especifica cómo valida el motor de representación los nombres de archivo en tiempo de representación.</span><span class="sxs-lookup"><span data-stu-id="2d77a-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="2d77a-113">Normalmente, una aplicación DES llamará a estos métodos en lugar de crear directamente una instancia del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="2d77a-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="2d77a-114">Para obtener más información, consulte [uso del localizador de medios](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="2d77a-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="2d77a-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d77a-115">Members</span></span>

<span data-ttu-id="2d77a-116">La interfaz **IMediaLocator** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d77a-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d77a-117">**IMediaLocator** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d77a-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="2d77a-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d77a-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d77a-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d77a-119">Methods</span></span>

<span data-ttu-id="2d77a-120">La interfaz **IMediaLocator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2d77a-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="2d77a-121">Método</span><span class="sxs-lookup"><span data-stu-id="2d77a-121">Method</span></span>                                                     | <span data-ttu-id="2d77a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d77a-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2d77a-123">**AddFoundLocation**</span><span class="sxs-lookup"><span data-stu-id="2d77a-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="2d77a-124">Agrega un directorio a la caché de directorio.</span><span class="sxs-lookup"><span data-stu-id="2d77a-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="2d77a-125">**FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="2d77a-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="2d77a-126">Busca un archivo y, si lo logra, recupera la ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="2d77a-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d77a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d77a-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d77a-128">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2d77a-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d77a-129">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d77a-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d77a-130">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2d77a-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d77a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d77a-131">Requirements</span></span>



| <span data-ttu-id="2d77a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d77a-132">Requirement</span></span> | <span data-ttu-id="2d77a-133">Value</span><span class="sxs-lookup"><span data-stu-id="2d77a-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d77a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d77a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2d77a-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d77a-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d77a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d77a-136">Library</span></span><br/> | <dl> <span data-ttu-id="2d77a-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d77a-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
