---
title: Función MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indexa un archivo de recursos que pertenece a una aplicación de UWP. Deduce una lista de calificadores de recursos del parámetro filePath. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menús de la función MrmIndexFileAutoQualifiers y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149949"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="6bf99-106">MrmIndexFileAutoQualifiers función)</span><span class="sxs-lookup"><span data-stu-id="6bf99-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="6bf99-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6bf99-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bf99-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6bf99-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bf99-109">Indexa un archivo de recursos que pertenece a una aplicación de UWP.</span><span class="sxs-lookup"><span data-stu-id="6bf99-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="6bf99-110">Deduce una lista de calificadores de recursos del parámetro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="6bf99-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="6bf99-111">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="6bf99-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf99-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bf99-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="6bf99-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bf99-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bf99-114">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bf99-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf99-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="6bf99-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="6bf99-116">Identificador que identifica el indizador de recursos que indizará el archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bf99-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="6bf99-117">*filePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bf99-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf99-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6bf99-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="6bf99-119">Una ruta de acceso relativa a un archivo que contiene un recurso que desea indizar.</span><span class="sxs-lookup"><span data-stu-id="6bf99-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="6bf99-120">Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI.</span><span class="sxs-lookup"><span data-stu-id="6bf99-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="6bf99-121">Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="6bf99-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bf99-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bf99-122">Return value</span></span>

<span data-ttu-id="6bf99-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6bf99-123">Type: **HRESULT**</span></span>

<span data-ttu-id="6bf99-124">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="6bf99-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="6bf99-125">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6bf99-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bf99-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bf99-126">Remarks</span></span>

<span data-ttu-id="6bf99-127">El segmento de nombre de archivo de *filePath* se usa como el nombre del recurso; y los calificadores de recursos se derivan de su ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6bf99-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="6bf99-128">Por ejemplo, si se pasa L "images \\ de-de \\ scale-100 \\background.png" a *filePath* , el indexador de recursos agrega un recurso denominado "background.png" con los calificadores de recursos "Language-de-de-de" y "Scale-100".</span><span class="sxs-lookup"><span data-stu-id="6bf99-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="6bf99-129">L "files" se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bf99-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bf99-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bf99-130">Requirements</span></span>



| <span data-ttu-id="6bf99-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bf99-131">Requirement</span></span> | <span data-ttu-id="6bf99-132">Value</span><span class="sxs-lookup"><span data-stu-id="6bf99-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf99-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bf99-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf99-134">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bf99-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6bf99-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bf99-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf99-136">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="6bf99-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bf99-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bf99-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bf99-138"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bf99-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="6bf99-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bf99-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bf99-140"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bf99-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="6bf99-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6bf99-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf99-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bf99-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6bf99-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bf99-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf99-144">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="6bf99-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

