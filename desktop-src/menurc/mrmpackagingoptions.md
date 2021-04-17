---
title: Enumeración MrmPackagingOptions (MrmResourceIndexer. h)
description: Define constantes que especifican las opciones para el archivo PRI creado por MrmCreateResourceFile y MrmCreateResourceFileInMemory.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Menús de enumeración de MrmPackagingOptions y otros recursos
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714535"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="10957-104">Enumeración MrmPackagingOptions</span><span class="sxs-lookup"><span data-stu-id="10957-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="10957-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="10957-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="10957-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="10957-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="10957-107">Define constantes que especifican las opciones para el archivo PRI creado por [**MrmCreateResourceFile**](mrmcreateresourcefile.md) y [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="10957-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="10957-108">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="10957-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="10957-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10957-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="10957-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="10957-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="10957-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span><span class="sxs-lookup"><span data-stu-id="10957-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="10957-112">No especifica ninguna opción de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="10957-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="10957-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span><span class="sxs-lookup"><span data-stu-id="10957-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="10957-114">Especifica que debe crearse un paquete de recursos sin esquema.</span><span class="sxs-lookup"><span data-stu-id="10957-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="10957-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span><span class="sxs-lookup"><span data-stu-id="10957-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="10957-116">Especifica que el archivo PRI debe dividirse automáticamente por todos los calificadores admitidos (específicamente, de idioma y de escala).</span><span class="sxs-lookup"><span data-stu-id="10957-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10957-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10957-117">Requirements</span></span>



| <span data-ttu-id="10957-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10957-118">Requirement</span></span> | <span data-ttu-id="10957-119">Value</span><span class="sxs-lookup"><span data-stu-id="10957-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10957-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10957-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10957-121">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="10957-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="10957-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10957-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10957-123">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="10957-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="10957-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10957-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10957-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="10957-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10957-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="10957-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10957-127">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="10957-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

