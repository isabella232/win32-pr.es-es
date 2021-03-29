---
title: Función MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria), para que sea más fácil de leer.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menús de la función MrmDumpPriFileInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665922"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="32d65-104">MrmDumpPriFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="32d65-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="32d65-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="32d65-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32d65-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="32d65-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32d65-107">Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria), para que sea más fácil de leer.</span><span class="sxs-lookup"><span data-stu-id="32d65-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="32d65-108">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="32d65-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="32d65-109">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="32d65-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="32d65-110">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="32d65-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="32d65-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32d65-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="32d65-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32d65-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d65-113">*indexFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32d65-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-114">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="32d65-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="32d65-115">Ruta de acceso completa a un archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="32d65-115">A full file path to a PRI file.</span></span> <span data-ttu-id="32d65-116">Este es el archivo PRI que se volcará en XML.</span><span class="sxs-lookup"><span data-stu-id="32d65-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="32d65-117">*schemaPriFile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="32d65-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="32d65-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="32d65-119">Una ruta de acceso de archivo completa opcional a un archivo de esquema (o a un archivo PRI que representa un esquema; vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="32d65-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="32d65-120">*dumpType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32d65-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-121">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="32d65-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="32d65-122">Especifica el grado de detalle del volcado XML o de si se debe volcar un esquema.</span><span class="sxs-lookup"><span data-stu-id="32d65-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="32d65-123">*outputXmlData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32d65-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="32d65-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="32d65-125">Dirección de un puntero a BYTE.</span><span class="sxs-lookup"><span data-stu-id="32d65-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="32d65-126">La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="32d65-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="32d65-127">Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="32d65-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="32d65-128">*outputXmlSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32d65-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-129">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="32d65-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="32d65-130">Dirección de un ULONG.</span><span class="sxs-lookup"><span data-stu-id="32d65-130">The address of a ULONG.</span></span> <span data-ttu-id="32d65-131">En _outputXmlSize \*, la función devuelve el tamaño de la memoria asignada a la que apunta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="32d65-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d65-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32d65-132">Return value</span></span>

<span data-ttu-id="32d65-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="32d65-133">Type: **HRESULT**</span></span>

<span data-ttu-id="32d65-134">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="32d65-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="32d65-135">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="32d65-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="32d65-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32d65-136">Remarks</span></span>

<span data-ttu-id="32d65-137">Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el modificador *OMITSCHEMAFROMRESOURCEPACKS* en el archivo de configuración de PRI).</span><span class="sxs-lookup"><span data-stu-id="32d65-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="32d65-138">Para volcar un paquete de recursos sin esquemas, pase la ruta de acceso a los datos del paquete principal de PRI como argumento para el parámetro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="32d65-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="32d65-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32d65-139">Requirements</span></span>



| <span data-ttu-id="32d65-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d65-140">Requirement</span></span> | <span data-ttu-id="32d65-141">Value</span><span class="sxs-lookup"><span data-stu-id="32d65-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d65-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32d65-142">Minimum supported client</span></span><br/> | <span data-ttu-id="32d65-143">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="32d65-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="32d65-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32d65-144">Minimum supported server</span></span><br/> | <span data-ttu-id="32d65-145">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="32d65-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="32d65-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32d65-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="32d65-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d65-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="32d65-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32d65-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="32d65-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32d65-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="32d65-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32d65-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32d65-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32d65-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="32d65-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="32d65-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d65-153">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="32d65-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

