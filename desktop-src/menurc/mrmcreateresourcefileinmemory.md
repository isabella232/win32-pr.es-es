---
title: Función MrmCreateResourceFileInMemory (MrmResourceIndexer. h)
description: Crea la información de PRI como un BLOB en la memoria, no como un archivo en disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menús de la función MrmCreateResourceFileInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492544"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="fadee-104">MrmCreateResourceFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="fadee-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="fadee-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fadee-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fadee-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fadee-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fadee-107">Crea la información de PRI como un BLOB en la memoria, no como un archivo en disco.</span><span class="sxs-lookup"><span data-stu-id="fadee-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="fadee-108">La función asigna memoria y devuelve un puntero a esa memoria en *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="fadee-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="fadee-109">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="fadee-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="fadee-110">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="fadee-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="fadee-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fadee-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="fadee-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fadee-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fadee-113">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fadee-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fadee-114">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="fadee-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="fadee-115">Identificador que identifica el indizador de recursos a partir del que se va a crear la información de PRI.</span><span class="sxs-lookup"><span data-stu-id="fadee-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="fadee-116">*packagingMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fadee-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fadee-117">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="fadee-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="fadee-118">Especifica si la información de PRI debe ser independiente o ser un paquete de recursos.</span><span class="sxs-lookup"><span data-stu-id="fadee-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="fadee-119">No se admite **MrmPackagingModeAutoSplit** .</span><span class="sxs-lookup"><span data-stu-id="fadee-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fadee-120">*packagingOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fadee-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fadee-121">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="fadee-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="fadee-122">Especifica opciones adicionales sobre la información de PRI.</span><span class="sxs-lookup"><span data-stu-id="fadee-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="fadee-123">*outputPriData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fadee-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fadee-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="fadee-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="fadee-125">Dirección de un puntero a BYTE.</span><span class="sxs-lookup"><span data-stu-id="fadee-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="fadee-126">La función asigna memoria y devuelve un puntero a esa memoria en *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="fadee-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="fadee-127">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="fadee-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="fadee-128">*outputPriSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fadee-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fadee-129">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="fadee-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="fadee-130">Dirección de un ULONG.</span><span class="sxs-lookup"><span data-stu-id="fadee-130">The address of a ULONG.</span></span> <span data-ttu-id="fadee-131">En _outputPriSize \*, la función devuelve el tamaño de la memoria asignada a la que apunta *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="fadee-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fadee-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fadee-132">Return value</span></span>

<span data-ttu-id="fadee-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fadee-133">Type: **HRESULT**</span></span>

<span data-ttu-id="fadee-134">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="fadee-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="fadee-135">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="fadee-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="fadee-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fadee-136">Remarks</span></span>

<span data-ttu-id="fadee-137">Si pasa *outputPriData* a [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), no libere memoria hasta que haya terminado de usar el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="fadee-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fadee-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fadee-138">Requirements</span></span>



| <span data-ttu-id="fadee-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fadee-139">Requirement</span></span> | <span data-ttu-id="fadee-140">Value</span><span class="sxs-lookup"><span data-stu-id="fadee-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fadee-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fadee-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fadee-142">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="fadee-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fadee-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fadee-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fadee-144">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="fadee-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fadee-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fadee-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fadee-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fadee-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="fadee-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fadee-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="fadee-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fadee-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="fadee-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fadee-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fadee-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fadee-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fadee-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fadee-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fadee-152">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="fadee-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

