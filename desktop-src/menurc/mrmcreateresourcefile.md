---
title: Función MrmCreateResourceFile (MrmResourceIndexer. h)
description: Crea un archivo PRI (denominado \ 0034; Resources. PRI \ 0034;), o archivos, en el disco de la carpeta especificada. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menús de la función MrmCreateResourceFile y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803446"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="013b3-105">MrmCreateResourceFile función)</span><span class="sxs-lookup"><span data-stu-id="013b3-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="013b3-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="013b3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="013b3-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="013b3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="013b3-108">Crea un archivo PRI (denominado "Resources. PRI") o archivos en el disco de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="013b3-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="013b3-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="013b3-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="013b3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="013b3-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="013b3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="013b3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="013b3-112">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="013b3-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="013b3-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="013b3-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="013b3-114">Identificador que identifica el indizador de recursos a partir del que se va a crear el archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="013b3-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="013b3-115">*packagingMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="013b3-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="013b3-116">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="013b3-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="013b3-117">Especifica si el archivo PRI debe ser independiente, dividirse automáticamente por el calificador de recursos o ser un paquete de recursos.</span><span class="sxs-lookup"><span data-stu-id="013b3-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="013b3-118">*packagingOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="013b3-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="013b3-119">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="013b3-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="013b3-120">Especifica opciones adicionales sobre el archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="013b3-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="013b3-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="013b3-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="013b3-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="013b3-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="013b3-123">Ruta de acceso a una carpeta en la que se va a guardar el archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="013b3-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="013b3-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="013b3-124">Return value</span></span>

<span data-ttu-id="013b3-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="013b3-125">Type: **HRESULT**</span></span>

<span data-ttu-id="013b3-126">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="013b3-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="013b3-127">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="013b3-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="013b3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="013b3-128">Requirements</span></span>



| <span data-ttu-id="013b3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="013b3-129">Requirement</span></span> | <span data-ttu-id="013b3-130">Value</span><span class="sxs-lookup"><span data-stu-id="013b3-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="013b3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="013b3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="013b3-132">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="013b3-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="013b3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="013b3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="013b3-134">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="013b3-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="013b3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="013b3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="013b3-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="013b3-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="013b3-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="013b3-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="013b3-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="013b3-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="013b3-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="013b3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="013b3-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="013b3-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="013b3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="013b3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013b3-142">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="013b3-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

