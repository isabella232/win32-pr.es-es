---
title: Función MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indexa los recursos de cadena incluidos en un archivo de recursos (. resw/. resjson) o un. priinfo o. prifile, que pertenece a una aplicación de UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menús de la función MrmIndexResourceContainerAutoQualifiers y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714611"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="81a10-104">MrmIndexResourceContainerAutoQualifiers función)</span><span class="sxs-lookup"><span data-stu-id="81a10-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="81a10-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="81a10-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="81a10-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="81a10-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="81a10-107">Indexa los recursos de cadena incluidos en un archivo de recursos (. resw/. resjson) o un. priinfo o. prifile, que pertenece a una aplicación de UWP.</span><span class="sxs-lookup"><span data-stu-id="81a10-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="81a10-108">Deduce una lista de calificadores de recursos del parámetro *containerPath* .</span><span class="sxs-lookup"><span data-stu-id="81a10-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="81a10-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="81a10-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="81a10-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81a10-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="81a10-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81a10-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a10-112">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81a10-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a10-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="81a10-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="81a10-114">Identificador que identifica el indizador de recursos que indizará los recursos de cadena.</span><span class="sxs-lookup"><span data-stu-id="81a10-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="81a10-115">*containerPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81a10-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a10-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="81a10-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="81a10-117">Una ruta de acceso relativa a un. resw,. resjson,. priinfo o. prifile que contiene los recursos de cadena que desea indizar.</span><span class="sxs-lookup"><span data-stu-id="81a10-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="81a10-118">Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="81a10-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="81a10-119">Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="81a10-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a10-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81a10-120">Return value</span></span>

<span data-ttu-id="81a10-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="81a10-121">Type: **HRESULT**</span></span>

<span data-ttu-id="81a10-122">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="81a10-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="81a10-123">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="81a10-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a10-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81a10-124">Remarks</span></span>

<span data-ttu-id="81a10-125">Los calificadores de recursos se deducen de *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="81a10-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="81a10-126">Por ejemplo, un valor de L "en-US \\ \\ Resources. resw" agrega recursos de cadena con el calificador "Language-en-US".</span><span class="sxs-lookup"><span data-stu-id="81a10-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="81a10-127">El nombre del archivo de recursos se usará como el nombre del subárbol del mapa de recursos para estos recursos cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="81a10-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a10-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a10-128">Requirements</span></span>



| <span data-ttu-id="81a10-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a10-129">Requirement</span></span> | <span data-ttu-id="81a10-130">Value</span><span class="sxs-lookup"><span data-stu-id="81a10-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a10-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a10-131">Minimum supported client</span></span><br/> | <span data-ttu-id="81a10-132">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="81a10-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="81a10-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a10-133">Minimum supported server</span></span><br/> | <span data-ttu-id="81a10-134">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="81a10-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="81a10-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81a10-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a10-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a10-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="81a10-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81a10-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="81a10-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a10-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="81a10-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81a10-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a10-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a10-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="81a10-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="81a10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a10-142">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="81a10-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

