---
title: Función MrmIndexFile (MrmResourceIndexer. h)
description: Indexa un archivo de recursos que pertenece a una aplicación de UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menús de la función MrmIndexFile y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492538"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="fb926-106">MrmIndexFile función)</span><span class="sxs-lookup"><span data-stu-id="fb926-106">MrmIndexFile function</span></span>

<span data-ttu-id="fb926-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fb926-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb926-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fb926-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb926-109">Indexa un archivo de recursos que pertenece a una aplicación de UWP.</span><span class="sxs-lookup"><span data-stu-id="fb926-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="fb926-110">Toma una lista explícita (pero opcional) de calificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb926-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="fb926-111">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="fb926-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb926-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb926-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="fb926-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb926-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb926-114">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb926-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb926-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="fb926-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="fb926-116">Identificador que identifica el indizador de recursos que indizará el archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb926-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="fb926-117">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb926-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb926-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="fb926-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="fb926-119">URI de recurso que se va a asignar al recurso.</span><span class="sxs-lookup"><span data-stu-id="fb926-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="fb926-120">La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb926-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="fb926-121">*filePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb926-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb926-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="fb926-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="fb926-123">Una ruta de acceso relativa a un archivo que contiene un recurso que desea indizar.</span><span class="sxs-lookup"><span data-stu-id="fb926-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="fb926-124">Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="fb926-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="fb926-125">Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="fb926-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb926-126">*calificadores* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fb926-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb926-127">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="fb926-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="fb926-128">Una lista opcional de calificadores de recursos, por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="fb926-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="fb926-129">Una cadena vacía o **nullptr** indica un recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="fb926-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="fb926-130">Los calificadores de recursos *no* se deducen de *ResourceUri* ni de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="fb926-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb926-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb926-131">Return value</span></span>

<span data-ttu-id="fb926-132">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fb926-132">Type: **HRESULT**</span></span>

<span data-ttu-id="fb926-133">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="fb926-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="fb926-134">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="fb926-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb926-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb926-135">Remarks</span></span>

<span data-ttu-id="fb926-136">Si desea especificar los calificadores de recursos, páselo en el parámetro *calificadores* .</span><span class="sxs-lookup"><span data-stu-id="fb926-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="fb926-137">Los calificadores de recursos *no* se deducen de *ResourceUri* ni de *filePath*.</span><span class="sxs-lookup"><span data-stu-id="fb926-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="fb926-138">El segmento de nombre de archivo de *resourceUri* (no *filePath*) se usa como nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="fb926-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb926-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb926-139">Requirements</span></span>



| <span data-ttu-id="fb926-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb926-140">Requirement</span></span> | <span data-ttu-id="fb926-141">Value</span><span class="sxs-lookup"><span data-stu-id="fb926-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb926-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb926-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fb926-143">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb926-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fb926-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb926-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fb926-145">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="fb926-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb926-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb926-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb926-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb926-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="fb926-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb926-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb926-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb926-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="fb926-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb926-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb926-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb926-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fb926-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb926-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb926-153">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="fb926-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

