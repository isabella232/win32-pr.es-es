---
title: Enumeración MrmPackagingMode (MrmResourceIndexer. h)
description: Define constantes que especifican qué tipo de archivos PRI debe crear MrmCreateResourceFile y MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menús de enumeración de MrmPackagingMode y otros recursos
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359746"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="561d3-104">Enumeración MrmPackagingMode</span><span class="sxs-lookup"><span data-stu-id="561d3-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="561d3-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="561d3-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="561d3-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="561d3-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="561d3-107">Define constantes que especifican qué tipo de archivos PRI debe crear [**MrmCreateResourceFile**](mrmcreateresourcefile.md) y [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="561d3-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="561d3-108">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="561d3-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="561d3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="561d3-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="561d3-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="561d3-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="561d3-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span><span class="sxs-lookup"><span data-stu-id="561d3-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="561d3-112">Especifica que debe crearse un único archivo PRI.</span><span class="sxs-lookup"><span data-stu-id="561d3-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="561d3-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span><span class="sxs-lookup"><span data-stu-id="561d3-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="561d3-114">Especifica que deben crearse varios archivos PRI; se divide automáticamente por todos los calificadores admitidos (específicamente, de idioma y de escala).</span><span class="sxs-lookup"><span data-stu-id="561d3-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="561d3-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span><span class="sxs-lookup"><span data-stu-id="561d3-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="561d3-116">Especifica que debe crearse un archivo PRI de satélite de complementos.</span><span class="sxs-lookup"><span data-stu-id="561d3-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="561d3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="561d3-117">Requirements</span></span>



| <span data-ttu-id="561d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="561d3-118">Requirement</span></span> | <span data-ttu-id="561d3-119">Value</span><span class="sxs-lookup"><span data-stu-id="561d3-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="561d3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="561d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="561d3-121">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="561d3-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="561d3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="561d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="561d3-123">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="561d3-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="561d3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="561d3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="561d3-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="561d3-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="561d3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="561d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561d3-127">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="561d3-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

