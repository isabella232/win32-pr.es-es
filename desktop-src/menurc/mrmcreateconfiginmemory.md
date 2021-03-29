---
title: Función MrmCreateConfigInMemory (MrmResourceIndexer. h)
description: Crea una nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menús de la función MrmCreateConfigInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535080"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="0f5ad-104">MrmCreateConfigInMemory función)</span><span class="sxs-lookup"><span data-stu-id="0f5ad-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="0f5ad-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f5ad-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f5ad-107">Crea una nueva información de configuración de PRI inicializada (como datos en memoria, no como un archivo) que define los valores predeterminados del calificador que especifique.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="0f5ad-108">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="0f5ad-109">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="0f5ad-110">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0f5ad-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ad-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f5ad-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="0f5ad-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f5ad-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5ad-113">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ad-114">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="0f5ad-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="0f5ad-115">Versión de la plataforma (*targetOsVersion*) que se va a usar para la información de configuración generada.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ad-116">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ad-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0f5ad-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f5ad-118">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="0f5ad-119">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="0f5ad-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="0f5ad-120">*outputXmlData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ad-121">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="0f5ad-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="0f5ad-122">Dirección de un puntero a BYTE.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="0f5ad-123">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="0f5ad-124">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ad-125">*outputXmlSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ad-126">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="0f5ad-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="0f5ad-127">Dirección de un ULONG.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-127">The address of a ULONG.</span></span> <span data-ttu-id="0f5ad-128">En _outputXmlSize \*, la función devuelve el tamaño de la memoria asignada a la que apunta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5ad-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f5ad-129">Return value</span></span>

<span data-ttu-id="0f5ad-130">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f5ad-130">Type: **HRESULT**</span></span>

<span data-ttu-id="0f5ad-131">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0f5ad-132">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="0f5ad-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5ad-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f5ad-133">Requirements</span></span>



| <span data-ttu-id="0f5ad-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f5ad-134">Requirement</span></span> | <span data-ttu-id="0f5ad-135">Value</span><span class="sxs-lookup"><span data-stu-id="0f5ad-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ad-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f5ad-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5ad-137">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f5ad-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f5ad-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5ad-139">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="0f5ad-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f5ad-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f5ad-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5ad-141"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ad-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0f5ad-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f5ad-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f5ad-143"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ad-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0f5ad-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f5ad-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5ad-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ad-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0f5ad-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f5ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ad-147">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="0f5ad-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

