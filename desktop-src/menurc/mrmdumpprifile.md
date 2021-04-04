---
title: Función MrmDumpPriFile (MrmResourceIndexer. h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco), con el fin de que sea más fácil de leer.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menús de la función MrmDumpPriFile y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802521"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="a1431-104">MrmDumpPriFile función)</span><span class="sxs-lookup"><span data-stu-id="a1431-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="a1431-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a1431-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a1431-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a1431-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a1431-107">Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco), con el fin de que sea más fácil de leer.</span><span class="sxs-lookup"><span data-stu-id="a1431-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="a1431-108">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="a1431-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1431-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1431-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="a1431-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1431-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1431-111">*indexFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1431-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1431-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1431-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1431-113">Ruta de acceso completa a un archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="a1431-113">A full file path to a PRI file.</span></span> <span data-ttu-id="a1431-114">Este es el archivo PRI que se volcará en XML.</span><span class="sxs-lookup"><span data-stu-id="a1431-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="a1431-115">*schemaPriFile* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a1431-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1431-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1431-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1431-117">Una ruta de acceso de archivo completa opcional a un archivo de esquema (o a un archivo PRI que representa un esquema; vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="a1431-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="a1431-118">*dumpType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1431-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1431-119">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="a1431-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="a1431-120">Especifica el grado de detalle del volcado XML o de si se debe volcar un esquema.</span><span class="sxs-lookup"><span data-stu-id="a1431-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="a1431-121">*outputXmlFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1431-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1431-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1431-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1431-123">Ruta de acceso de un archivo XML que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="a1431-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1431-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1431-124">Return value</span></span>

<span data-ttu-id="a1431-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a1431-125">Type: **HRESULT**</span></span>

<span data-ttu-id="a1431-126">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="a1431-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="a1431-127">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="a1431-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1431-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1431-128">Remarks</span></span>

<span data-ttu-id="a1431-129">Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el modificador *OMITSCHEMAFROMRESOURCEPACKS* en el archivo de configuración de PRI).</span><span class="sxs-lookup"><span data-stu-id="a1431-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="a1431-130">Para volcar un paquete de recursos sin esquemas, pase la ruta de acceso a los datos del paquete principal de PRI como argumento para el parámetro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="a1431-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1431-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1431-131">Requirements</span></span>



| <span data-ttu-id="a1431-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1431-132">Requirement</span></span> | <span data-ttu-id="a1431-133">Value</span><span class="sxs-lookup"><span data-stu-id="a1431-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1431-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1431-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a1431-135">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1431-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a1431-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1431-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a1431-137">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="a1431-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1431-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1431-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1431-139"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1431-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="a1431-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1431-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1431-141"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1431-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="a1431-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1431-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1431-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1431-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a1431-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1431-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1431-145">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="a1431-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

