---
title: Función MrmIndexEmbeddedData (MrmResourceIndexer. h)
description: Indexa un único recurso de datos insertado que pertenece a una aplicación de UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menús de la función MrmIndexEmbeddedData y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665921"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="e58a4-104">MrmIndexEmbeddedData función)</span><span class="sxs-lookup"><span data-stu-id="e58a4-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="e58a4-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e58a4-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e58a4-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e58a4-107">Indexa un único recurso de **datos insertado** que pertenece a una aplicación de UWP.</span><span class="sxs-lookup"><span data-stu-id="e58a4-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="e58a4-108">Toma una lista explícita (pero opcional) de calificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="e58a4-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="e58a4-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e58a4-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e58a4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e58a4-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="e58a4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e58a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58a4-112">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58a4-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="e58a4-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="e58a4-114">Identificador que identifica el indizador de recursos que indizará el archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e58a4-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="e58a4-115">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58a4-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e58a4-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="e58a4-117">URI de recurso que se va a asignar al recurso.</span><span class="sxs-lookup"><span data-stu-id="e58a4-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="e58a4-118">La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e58a4-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="e58a4-119">*datos insertado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58a4-120">Tipo: \**const byte \** _</span><span class="sxs-lookup"><span data-stu-id="e58a4-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="e58a4-121">Un puntero a los datos del recurso que desea indizar.</span><span class="sxs-lookup"><span data-stu-id="e58a4-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="e58a4-122">_embeddedDataSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58a4-123">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="e58a4-123">Type: **ULONG**</span></span>

<span data-ttu-id="e58a4-124">Tamaño de los datos a los que apunta *datos insertado*.</span><span class="sxs-lookup"><span data-stu-id="e58a4-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="e58a4-125">*calificadores* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e58a4-126">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e58a4-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="e58a4-127">Una lista opcional de calificadores de recursos, por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="e58a4-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="e58a4-128">Una cadena vacía o **nullptr** indica un recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="e58a4-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="e58a4-129">Los calificadores de recursos *no* se deducen de *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="e58a4-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58a4-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e58a4-130">Return value</span></span>

<span data-ttu-id="e58a4-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e58a4-131">Type: **HRESULT**</span></span>

<span data-ttu-id="e58a4-132">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="e58a4-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e58a4-133">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="e58a4-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e58a4-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e58a4-134">Remarks</span></span>

<span data-ttu-id="e58a4-135">Si desea especificar los calificadores de recursos, páselo en el parámetro *calificadores* .</span><span class="sxs-lookup"><span data-stu-id="e58a4-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="e58a4-136">Los calificadores de recursos *no* se deducen de *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="e58a4-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="e58a4-137">El segmento de nombre de archivo de *resourceUri* se usa como nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="e58a4-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58a4-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58a4-138">Requirements</span></span>



| <span data-ttu-id="e58a4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58a4-139">Requirement</span></span> | <span data-ttu-id="e58a4-140">Value</span><span class="sxs-lookup"><span data-stu-id="e58a4-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58a4-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58a4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e58a4-142">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e58a4-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58a4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e58a4-144">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="e58a4-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e58a4-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e58a4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58a4-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58a4-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e58a4-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e58a4-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="e58a4-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e58a4-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e58a4-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e58a4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e58a4-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e58a4-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e58a4-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e58a4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58a4-152">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="e58a4-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

