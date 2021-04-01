---
title: Función MrmIndexString (MrmResourceIndexer. h)
description: Indexa un recurso de cadena único que pertenece a una aplicación de UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menús de la función MrmIndexString y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149948"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="79612-104">MrmIndexString función)</span><span class="sxs-lookup"><span data-stu-id="79612-104">MrmIndexString function</span></span>

<span data-ttu-id="79612-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="79612-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="79612-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="79612-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="79612-107">Indexa un recurso de cadena único que pertenece a una aplicación de UWP.</span><span class="sxs-lookup"><span data-stu-id="79612-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="79612-108">Toma una lista explícita (pero opcional) de calificadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="79612-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="79612-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="79612-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="79612-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79612-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="79612-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79612-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79612-112">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79612-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79612-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="79612-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="79612-114">Identificador que identifica el indizador de recursos que indizará los recursos de cadena.</span><span class="sxs-lookup"><span data-stu-id="79612-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="79612-115">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79612-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79612-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="79612-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="79612-117">URI de recurso que se va a asignar al recurso.</span><span class="sxs-lookup"><span data-stu-id="79612-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="79612-118">La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="79612-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="79612-119">*resourceString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79612-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79612-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="79612-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="79612-121">Valor del recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="79612-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="79612-122">*calificadores* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="79612-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79612-123">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="79612-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="79612-124">Una lista opcional de calificadores de recursos, por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard".</span><span class="sxs-lookup"><span data-stu-id="79612-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="79612-125">Una cadena vacía o **nullptr** indica un recurso neutro.</span><span class="sxs-lookup"><span data-stu-id="79612-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="79612-126">Los calificadores de recursos *no* se deducen de *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="79612-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79612-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79612-127">Return value</span></span>

<span data-ttu-id="79612-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79612-128">Type: **HRESULT**</span></span>

<span data-ttu-id="79612-129">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="79612-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="79612-130">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="79612-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="79612-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79612-131">Remarks</span></span>

<span data-ttu-id="79612-132">Si desea especificar los calificadores de recursos, páselo en el parámetro *calificadores* .</span><span class="sxs-lookup"><span data-stu-id="79612-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="79612-133">Los calificadores de recursos *no* se deducen de *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="79612-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="79612-134">El segmento de nombre de archivo de *resourceUri* se usa como nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="79612-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="79612-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79612-135">Requirements</span></span>



| <span data-ttu-id="79612-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="79612-136">Requirement</span></span> | <span data-ttu-id="79612-137">Value</span><span class="sxs-lookup"><span data-stu-id="79612-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79612-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79612-138">Minimum supported client</span></span><br/> | <span data-ttu-id="79612-139">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="79612-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="79612-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79612-140">Minimum supported server</span></span><br/> | <span data-ttu-id="79612-141">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="79612-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79612-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79612-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="79612-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="79612-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="79612-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79612-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="79612-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79612-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="79612-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79612-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79612-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79612-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="79612-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="79612-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79612-149">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="79612-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

