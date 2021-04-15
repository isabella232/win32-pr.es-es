---
title: Función MrmCreateResourceIndexerFromPreviousPriFile (MrmResourceIndexer. h)
description: Crea un indizador de recursos a partir de un archivo PRI creado con una llamada anterior a MrmCreateResourceFile. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousPriFile y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666009"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a><span data-ttu-id="3d371-105">MrmCreateResourceIndexerFromPreviousPriFile función)</span><span class="sxs-lookup"><span data-stu-id="3d371-105">MrmCreateResourceIndexerFromPreviousPriFile function</span></span>

<span data-ttu-id="3d371-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3d371-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3d371-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3d371-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3d371-108">Crea un indizador de recursos a partir de un archivo PRI creado con una llamada anterior a [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span><span class="sxs-lookup"><span data-stu-id="3d371-108">Creates a resource indexer from a PRI file created with a previous call to [**MrmCreateResourceFile**](mrmcreateresourcefile.md).</span></span> <span data-ttu-id="3d371-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="3d371-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d371-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d371-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="3d371-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d371-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d371-112">*projectRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3d371-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d371-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d371-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="3d371-114">La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="3d371-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="3d371-115">En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="3d371-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="3d371-116">Especifique esto para que pueda especificar las rutas de acceso relativas a esa raíz en las posteriores llamadas API al mismo indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d371-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="3d371-117">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3d371-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d371-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="3d371-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="3d371-119">Versión de la plataforma de destino para el indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d371-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="3d371-120">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3d371-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d371-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d371-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="3d371-122">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3d371-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="3d371-123">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="3d371-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="3d371-124">*priFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3d371-124">*priFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d371-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3d371-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="3d371-126">Ruta de acceso completa a un archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="3d371-126">A full file path to a PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="3d371-127">*indexador* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d371-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d371-128">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="3d371-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="3d371-129">Un puntero a un identificador de indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d371-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d371-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d371-130">Return value</span></span>

<span data-ttu-id="3d371-131">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3d371-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3d371-132">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="3d371-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="3d371-133">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="3d371-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d371-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d371-134">Requirements</span></span>



| <span data-ttu-id="3d371-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d371-135">Requirement</span></span> | <span data-ttu-id="3d371-136">Value</span><span class="sxs-lookup"><span data-stu-id="3d371-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d371-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d371-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3d371-138">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d371-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3d371-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d371-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3d371-140">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="3d371-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3d371-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d371-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d371-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d371-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="3d371-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d371-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d371-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d371-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="3d371-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d371-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d371-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d371-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3d371-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d371-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d371-148">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="3d371-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

