---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Crea un objeto de generador que se usa para la creación posterior de objetos DWriteCore individuales.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 3ba1b8f6e09212c1ba2f4a0093e2205acaa2e835
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548940"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="9aad6-103">Función DWriteCoreCreateFactory (dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="9aad6-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="9aad6-104">Crea un objeto de generador que se usa para la creación posterior de objetos DWriteCore individuales.</span><span class="sxs-lookup"><span data-stu-id="9aad6-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9aad6-105">Esta API está disponible como parte de la implementación de DWriteCore [de DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="9aad6-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="9aad6-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="9aad6-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="9aad6-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="9aad6-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aad6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aad6-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="9aad6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aad6-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="9aad6-110">Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="9aad6-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="9aad6-111">Valor que especifica si el objeto de generador se compartirá, aislará o restringirá.</span><span class="sxs-lookup"><span data-stu-id="9aad6-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="9aad6-112">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="9aad6-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="9aad6-113">Valor GUID que identifica la interfaz del generador de DirectWrite, como __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="9aad6-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="9aad6-114">Tipo: <b>IUnknown\*\*</b></span><span class="sxs-lookup"><span data-stu-id="9aad6-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="9aad6-115">Dirección de un puntero al objeto de generador directWrite recién creado.</span><span class="sxs-lookup"><span data-stu-id="9aad6-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aad6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aad6-116">Return value</span></span>

<span data-ttu-id="9aad6-117">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="9aad6-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="9aad6-118">Si este método se realiza correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="9aad6-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="9aad6-119">De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="9aad6-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="9aad6-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9aad6-120">Examples</span></span>

<span data-ttu-id="9aad6-121">Consulte el tema [de información general de DWriteCore](../dwritecore-overview.md) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="9aad6-121">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aad6-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9aad6-122">Remarks</span></span>

<span data-ttu-id="9aad6-123">Esto es funcionalmente igual que la función [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada por la versión del sistema de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="9aad6-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="9aad6-124">La función DWriteCore tiene un nombre diferente para evitar ambigüedades.</span><span class="sxs-lookup"><span data-stu-id="9aad6-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aad6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aad6-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9aad6-126">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="9aad6-126">**Minimum supported client**</span></span> | <span data-ttu-id="9aad6-127">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="9aad6-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="9aad6-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="9aad6-128">**Header**</span></span> | <span data-ttu-id="9aad6-129">dwrite.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="9aad6-129">dwrite.h (include dwrite_core.h)</span></span> |