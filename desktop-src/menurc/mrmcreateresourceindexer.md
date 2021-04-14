---
title: Función MrmCreateResourceIndexer (MrmResourceIndexer. h)
description: Crea un indizador de recursos, que se usa para generar archivos de índice de recursos del paquete (PRI) para una aplicación para UWP. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menús de la función MrmCreateResourceIndexer y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422545"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="451db-105">MrmCreateResourceIndexer función)</span><span class="sxs-lookup"><span data-stu-id="451db-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="451db-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="451db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="451db-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="451db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="451db-108">Crea un indizador de recursos, que se usa para generar archivos de índice de recursos del paquete (PRI) para una aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="451db-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="451db-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="451db-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="451db-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="451db-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="451db-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="451db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451db-112">*packageFamilyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="451db-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451db-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="451db-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="451db-114">El nombre de familia de paquete de la aplicación para UWP para la que va a generar archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="451db-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="451db-115">Este valor se usará como nombre del mapa de recursos cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="451db-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="451db-116">*projectRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="451db-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451db-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="451db-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="451db-118">La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="451db-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="451db-119">En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="451db-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="451db-120">Especifique esto para que pueda especificar las rutas de acceso relativas a esa raíz en las posteriores llamadas API al mismo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="451db-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="451db-121">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="451db-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451db-122">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="451db-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="451db-123">Versión de la plataforma de destino para el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="451db-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="451db-124">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="451db-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="451db-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="451db-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="451db-126">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="451db-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="451db-127">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="451db-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="451db-128">*indexador* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="451db-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="451db-129">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="451db-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="451db-130">Un puntero a un identificador de indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="451db-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451db-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="451db-131">Return value</span></span>

<span data-ttu-id="451db-132">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="451db-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="451db-133">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="451db-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="451db-134">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="451db-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="451db-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451db-135">Requirements</span></span>



| <span data-ttu-id="451db-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="451db-136">Requirement</span></span> | <span data-ttu-id="451db-137">Value</span><span class="sxs-lookup"><span data-stu-id="451db-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451db-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="451db-138">Minimum supported client</span></span><br/> | <span data-ttu-id="451db-139">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="451db-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="451db-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="451db-140">Minimum supported server</span></span><br/> | <span data-ttu-id="451db-141">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="451db-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="451db-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="451db-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="451db-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="451db-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="451db-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="451db-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="451db-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="451db-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="451db-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="451db-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451db-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451db-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="451db-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="451db-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451db-149">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="451db-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

