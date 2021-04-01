---
title: Enumeración MrmPlatformVersion (MrmResourceIndexer. h)
description: Define constantes que especifican una versión de la plataforma. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Menús de enumeración de MrmPlatformVersion y otros recursos
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997035"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="89067-105">Enumeración MrmPlatformVersion</span><span class="sxs-lookup"><span data-stu-id="89067-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="89067-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="89067-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89067-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="89067-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89067-108">Define constantes que especifican una versión de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="89067-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="89067-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="89067-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="89067-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89067-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="89067-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="89067-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="89067-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**\_Valor predeterminado de MrmPlatformVersion**</span><span class="sxs-lookup"><span data-stu-id="89067-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="89067-113">Especifica que la versión de la plataforma es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89067-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="89067-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="89067-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="89067-115">Especifica una versión de plataforma de Windows 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="89067-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="89067-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="89067-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="89067-117">Especifica una versión de plataforma de Windows 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="89067-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89067-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89067-118">Requirements</span></span>



| <span data-ttu-id="89067-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="89067-119">Requirement</span></span> | <span data-ttu-id="89067-120">Value</span><span class="sxs-lookup"><span data-stu-id="89067-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89067-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89067-121">Minimum supported client</span></span><br/> | <span data-ttu-id="89067-122">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="89067-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="89067-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89067-123">Minimum supported server</span></span><br/> | <span data-ttu-id="89067-124">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="89067-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="89067-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89067-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="89067-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="89067-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89067-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="89067-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89067-128">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="89067-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

