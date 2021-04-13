---
title: Enumeración MrmDumpType (MrmResourceIndexer. h)
description: Define constantes que especifican el tipo de volcado de archivo PRI que se va a producir. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Menús de enumeración de MrmDumpType y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491044"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="ce5d8-105">Enumeración MrmDumpType</span><span class="sxs-lookup"><span data-stu-id="ce5d8-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="ce5d8-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ce5d8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce5d8-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ce5d8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce5d8-108">Define constantes que especifican el tipo de volcado de archivo PRI que se va a producir.</span><span class="sxs-lookup"><span data-stu-id="ce5d8-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="ce5d8-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ce5d8-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5d8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce5d8-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="ce5d8-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="ce5d8-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce5d8-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType \_ básico**</span><span class="sxs-lookup"><span data-stu-id="ce5d8-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="ce5d8-113">Especifica que el volcado debe ser básico.</span><span class="sxs-lookup"><span data-stu-id="ce5d8-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="ce5d8-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType \_ detallado**</span><span class="sxs-lookup"><span data-stu-id="ce5d8-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="ce5d8-115">Especifica que debe detallarse el volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="ce5d8-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="ce5d8-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**\_Esquema MrmDumpType**</span><span class="sxs-lookup"><span data-stu-id="ce5d8-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="ce5d8-117">Especifica que el volcado debe ser un esquema.</span><span class="sxs-lookup"><span data-stu-id="ce5d8-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce5d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce5d8-118">Requirements</span></span>



| <span data-ttu-id="ce5d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce5d8-119">Requirement</span></span> | <span data-ttu-id="ce5d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="ce5d8-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5d8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce5d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce5d8-122">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce5d8-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ce5d8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce5d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce5d8-124">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="ce5d8-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ce5d8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce5d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce5d8-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5d8-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5d8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce5d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5d8-128">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="ce5d8-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

