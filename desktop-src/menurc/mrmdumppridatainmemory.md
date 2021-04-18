---
title: Función MrmDumpPriDataInMemory (MrmResourceIndexer. h)
description: Vuelca la información de PRI (como un BLOB en memoria, creada por una llamada anterior a MrmCreateResourceFileInMemory) a su equivalente XML (como datos en memoria), para que sea más fácil de leer.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menús de la función MrmDumpPriDataInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666054"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="5933b-104">MrmDumpPriDataInMemory función)</span><span class="sxs-lookup"><span data-stu-id="5933b-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="5933b-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5933b-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5933b-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5933b-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5933b-107">Vuelca la información de PRI (como un BLOB en memoria, creada por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) a su equivalente XML (como datos en memoria), para que sea más fácil de leer.</span><span class="sxs-lookup"><span data-stu-id="5933b-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="5933b-108">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="5933b-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="5933b-109">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="5933b-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="5933b-110">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5933b-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5933b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5933b-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="5933b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5933b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5933b-113">*inputPriData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5933b-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-114">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="5933b-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="5933b-115">Un puntero a los datos de PRI creados por una llamada anterior a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="5933b-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5933b-116">*inputPriSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5933b-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-117">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="5933b-117">Type: **ULONG**</span></span>

<span data-ttu-id="5933b-118">Tamaño de los datos a los que apunta *inputPriData*.</span><span class="sxs-lookup"><span data-stu-id="5933b-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="5933b-119">*schemaPriData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5933b-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-120">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="5933b-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="5933b-121">Un puntero opcional a la información de PRI (como un BLOB en memoria) que representa los datos de esquema creados por una llamada anterior a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="5933b-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="5933b-122">No libere *schemaPriData* hasta que termine de usar el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="5933b-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="5933b-123">Vea también la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5933b-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5933b-124">*schemaPriSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5933b-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-125">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="5933b-125">Type: **ULONG**</span></span>

<span data-ttu-id="5933b-126">Tamaño de los datos a los que apunta *schemaPriData*.</span><span class="sxs-lookup"><span data-stu-id="5933b-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="5933b-127">*dumpType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5933b-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-128">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="5933b-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="5933b-129">Especifica el grado de detalle del volcado XML o de si se debe volcar un esquema.</span><span class="sxs-lookup"><span data-stu-id="5933b-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="5933b-130">*outputXmlData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5933b-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-131">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="5933b-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="5933b-132">Dirección de un puntero a BYTE.</span><span class="sxs-lookup"><span data-stu-id="5933b-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="5933b-133">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="5933b-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="5933b-134">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="5933b-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="5933b-135">*outputXmlSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5933b-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5933b-136">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="5933b-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="5933b-137">Dirección de un ULONG.</span><span class="sxs-lookup"><span data-stu-id="5933b-137">The address of a ULONG.</span></span> <span data-ttu-id="5933b-138">En _outputXmlSize \*, la función devuelve el tamaño de la memoria asignada a la que apunta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="5933b-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5933b-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5933b-139">Return value</span></span>

<span data-ttu-id="5933b-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5933b-140">Type: **HRESULT**</span></span>

<span data-ttu-id="5933b-141">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="5933b-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="5933b-142">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="5933b-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5933b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5933b-143">Remarks</span></span>

<span data-ttu-id="5933b-144">Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el modificador *OMITSCHEMAFROMRESOURCEPACKS* en el archivo de configuración de PRI).</span><span class="sxs-lookup"><span data-stu-id="5933b-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="5933b-145">Para volcar un paquete de recursos sin esquemas, pase la ruta de acceso a los datos del paquete principal de PRI como argumento para el parámetro *schemaPriData* .</span><span class="sxs-lookup"><span data-stu-id="5933b-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5933b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5933b-146">Requirements</span></span>



| <span data-ttu-id="5933b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5933b-147">Requirement</span></span> | <span data-ttu-id="5933b-148">Value</span><span class="sxs-lookup"><span data-stu-id="5933b-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5933b-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5933b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5933b-150">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="5933b-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5933b-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5933b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5933b-152">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="5933b-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5933b-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5933b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5933b-154"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5933b-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="5933b-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5933b-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="5933b-156"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5933b-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="5933b-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5933b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5933b-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5933b-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5933b-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="5933b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5933b-160">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="5933b-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

