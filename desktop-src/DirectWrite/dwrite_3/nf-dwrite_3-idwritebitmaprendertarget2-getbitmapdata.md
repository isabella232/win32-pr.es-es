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
ms.openlocfilehash: 3dbc87697750ee07939602dc694468aa68f5c66d
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881854"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="2ba09-103">Método IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="2ba09-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="2ba09-104">Recupera los datos de píxeles de un destino de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2ba09-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ba09-105">Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2ba09-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="2ba09-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="2ba09-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="2ba09-107">Para obtener más información y ejemplos de código, vea Introducción a [DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="2ba09-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ba09-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="2ba09-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ba09-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="2ba09-110">Tipo: \_ Salida \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ba09-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="2ba09-111">Puntero a los datos de píxel.</span><span class="sxs-lookup"><span data-stu-id="2ba09-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ba09-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ba09-112">Return value</span></span>

<span data-ttu-id="2ba09-113">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="2ba09-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="2ba09-114">Si este método se realiza correctamente, devuelve <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="2ba09-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="2ba09-115">De lo contrario, devuelve un código de error <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="2ba09-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="2ba09-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2ba09-116">Examples</span></span>

<span data-ttu-id="2ba09-117">Consulte el [tema de información general de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) y la aplicación de ejemplo [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="2ba09-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba09-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ba09-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2ba09-119">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="2ba09-119">**Minimum supported client**</span></span> | <span data-ttu-id="2ba09-120">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="2ba09-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="2ba09-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="2ba09-121">**Header**</span></span> | <span data-ttu-id="2ba09-122">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="2ba09-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="2ba09-123">**Library**</span><span class="sxs-lookup"><span data-stu-id="2ba09-123">**Library**</span></span> | <span data-ttu-id="2ba09-124">Dwrite.lib</span><span class="sxs-lookup"><span data-stu-id="2ba09-124">Dwrite.lib</span></span> |
| <span data-ttu-id="2ba09-125">**Dll**</span><span class="sxs-lookup"><span data-stu-id="2ba09-125">**DLL**</span></span> | <span data-ttu-id="2ba09-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="2ba09-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="2ba09-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2ba09-127">See also</span></span>

[<span data-ttu-id="2ba09-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="2ba09-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
