---
title: Función MrmCreateResourceIndexerFromPreviousPriData (MrmResourceIndexer. h)
description: Crea un indizador de recursos a partir de los datos de PRI creados por una llamada anterior a MrmCreateResourceFileInMemory. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousPriData y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359800"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="d86ce-105">MrmCreateResourceIndexerFromPreviousPriData función)</span><span class="sxs-lookup"><span data-stu-id="d86ce-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="d86ce-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d86ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d86ce-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d86ce-108">Crea un indizador de recursos a partir de los datos de PRI creados por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d86ce-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="d86ce-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="d86ce-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d86ce-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d86ce-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="d86ce-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d86ce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86ce-112">*projectRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d86ce-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="d86ce-114">La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="d86ce-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="d86ce-115">En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="d86ce-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="d86ce-116">Especifique esto para que pueda especificar las rutas de acceso relativas a esa raíz en las posteriores llamadas API al mismo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ce-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="d86ce-117">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="d86ce-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="d86ce-119">Versión de la plataforma de destino para el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ce-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="d86ce-120">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d86ce-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="d86ce-122">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="d86ce-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="d86ce-123">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="d86ce-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="d86ce-124">*priData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="d86ce-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="d86ce-126">Un puntero a los datos de PRI creados por una llamada anterior a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d86ce-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="d86ce-127">No libere *priData* hasta que termine de usar el indizador de recursos creado por esta función.</span><span class="sxs-lookup"><span data-stu-id="d86ce-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="d86ce-128">*Inprise* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-129">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="d86ce-129">Type: **ULONG**</span></span>

<span data-ttu-id="d86ce-130">Tamaño de los datos a los que apunta *priData*.</span><span class="sxs-lookup"><span data-stu-id="d86ce-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="d86ce-131">*indexador* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d86ce-132">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d86ce-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="d86ce-133">Un puntero a un identificador de indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ce-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86ce-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d86ce-134">Return value</span></span>

<span data-ttu-id="d86ce-135">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d86ce-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d86ce-136">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d86ce-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="d86ce-137">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d86ce-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86ce-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d86ce-138">Remarks</span></span>

<span data-ttu-id="d86ce-139">No libere *priData* hasta que termine de usar el indizador de recursos creado por esta función.</span><span class="sxs-lookup"><span data-stu-id="d86ce-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86ce-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d86ce-140">Requirements</span></span>



| <span data-ttu-id="d86ce-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86ce-141">Requirement</span></span> | <span data-ttu-id="d86ce-142">Value</span><span class="sxs-lookup"><span data-stu-id="d86ce-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86ce-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d86ce-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d86ce-144">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d86ce-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d86ce-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d86ce-146">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="d86ce-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d86ce-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d86ce-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d86ce-148"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86ce-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="d86ce-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d86ce-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="d86ce-150"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d86ce-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="d86ce-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d86ce-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d86ce-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d86ce-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d86ce-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="d86ce-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86ce-154">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="d86ce-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

