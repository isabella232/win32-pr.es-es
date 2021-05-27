---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Recupera los datos de píxeles de un destino de representación de mapa de bits.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550290"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="f7a1a-103">Método IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="f7a1a-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="f7a1a-104">Recupera los datos de píxeles de un destino de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="f7a1a-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7a1a-105">Esta API está disponible como parte de la implementación de DWriteCore [de DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f7a1a-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="f7a1a-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="f7a1a-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="f7a1a-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f7a1a-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a1a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7a1a-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="f7a1a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7a1a-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="f7a1a-110">Tipo: \_ Out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7a1a-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="f7a1a-111">Puntero a los datos de píxel.</span><span class="sxs-lookup"><span data-stu-id="f7a1a-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7a1a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7a1a-112">Return value</span></span>

<span data-ttu-id="f7a1a-113">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="f7a1a-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="f7a1a-114">Si este método se realiza correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="f7a1a-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="f7a1a-115">De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="f7a1a-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="f7a1a-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f7a1a-116">Examples</span></span>

<span data-ttu-id="f7a1a-117">Consulte el tema [de información general de DWriteCore](../dwritecore-overview.md) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="f7a1a-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a1a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7a1a-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f7a1a-119">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="f7a1a-119">**Minimum supported client**</span></span> | <span data-ttu-id="f7a1a-120">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="f7a1a-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="f7a1a-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="f7a1a-121">**Header**</span></span> | <span data-ttu-id="f7a1a-122">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="f7a1a-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="f7a1a-123">**Library**</span><span class="sxs-lookup"><span data-stu-id="f7a1a-123">**Library**</span></span> | <span data-ttu-id="f7a1a-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="f7a1a-124">Dwrite.lib</span></span> |
| <span data-ttu-id="f7a1a-125">**Dll**</span><span class="sxs-lookup"><span data-stu-id="f7a1a-125">**DLL**</span></span> | <span data-ttu-id="f7a1a-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="f7a1a-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="f7a1a-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7a1a-127">See also</span></span>

[<span data-ttu-id="f7a1a-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="f7a1a-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)