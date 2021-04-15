---
title: Función MrmCreateResourceIndexerFromPreviousSchemaData (MrmResourceIndexer. h)
description: Crea un indizador de recursos a partir de los datos de esquema en memoria creados con una llamada anterior a MrmDumpPriFileInMemory o MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousSchemaData y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491045"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="52868-104">MrmCreateResourceIndexerFromPreviousSchemaData función)</span><span class="sxs-lookup"><span data-stu-id="52868-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="52868-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="52868-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="52868-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="52868-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="52868-107">Crea un indizador de recursos a partir de los datos de esquema en memoria creados con una llamada anterior a [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="52868-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="52868-108">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="52868-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="52868-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52868-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="52868-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52868-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52868-111">*projectRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52868-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="52868-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="52868-113">La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="52868-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="52868-114">En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="52868-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="52868-115">Especifique esto para que pueda especificar las rutas de acceso relativas a esa raíz en las posteriores llamadas API al mismo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="52868-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="52868-116">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52868-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-117">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="52868-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="52868-118">Versión de la plataforma de destino para el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="52868-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="52868-119">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="52868-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="52868-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="52868-121">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="52868-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="52868-122">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="52868-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="52868-123">*schemaXmlData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52868-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-124">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="52868-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="52868-125">Un puntero a los datos del esquema creados por una llamada anterior a [_ *MrmDumpPriFileInMemory* \*](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="52868-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="52868-126">No libere *schemaXmlData* hasta que termine de usar el indizador de recursos creado por esta función.</span><span class="sxs-lookup"><span data-stu-id="52868-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="52868-127">*schemaXmlSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52868-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-128">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="52868-128">Type: **ULONG**</span></span>

<span data-ttu-id="52868-129">Tamaño de los datos a los que apunta *schemaXmlData*.</span><span class="sxs-lookup"><span data-stu-id="52868-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="52868-130">*indexador* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="52868-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52868-131">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="52868-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="52868-132">Un puntero a un identificador de indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="52868-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52868-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52868-133">Return value</span></span>

<span data-ttu-id="52868-134">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="52868-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="52868-135">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="52868-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="52868-136">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="52868-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="52868-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52868-137">Remarks</span></span>

<span data-ttu-id="52868-138">No libere *schemaXmlData* hasta que termine de usar el indizador de recursos creado por esta función.</span><span class="sxs-lookup"><span data-stu-id="52868-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="52868-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52868-139">Requirements</span></span>



| <span data-ttu-id="52868-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="52868-140">Requirement</span></span> | <span data-ttu-id="52868-141">Value</span><span class="sxs-lookup"><span data-stu-id="52868-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52868-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52868-142">Minimum supported client</span></span><br/> | <span data-ttu-id="52868-143">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="52868-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="52868-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52868-144">Minimum supported server</span></span><br/> | <span data-ttu-id="52868-145">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="52868-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="52868-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52868-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="52868-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="52868-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="52868-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52868-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="52868-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52868-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="52868-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52868-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52868-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52868-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="52868-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="52868-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52868-153">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="52868-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

