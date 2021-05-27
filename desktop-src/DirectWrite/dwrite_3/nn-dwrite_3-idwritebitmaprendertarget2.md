---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos.
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: 346b2e9c7510010abb50f421489b67f7d327512f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548950"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="4fa08-103">Interfaz IDWriteBitmapRenderTarget2 (dwrite_3.h)</span><span class="sxs-lookup"><span data-stu-id="4fa08-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="4fa08-104">Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos.</span><span class="sxs-lookup"><span data-stu-id="4fa08-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fa08-105">Esta API está disponible como parte de la implementación de DWriteCore de [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="4fa08-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="4fa08-106">DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.</span><span class="sxs-lookup"><span data-stu-id="4fa08-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="4fa08-107">Para obtener más información y ejemplos de código, vea [Introducción a DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4fa08-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="inheritance"></a><span data-ttu-id="4fa08-108">Herencia</span><span class="sxs-lookup"><span data-stu-id="4fa08-108">Inheritance</span></span>

<span data-ttu-id="4fa08-109">La **interfaz IDWriteBitmapRenderTarget2** hereda de [IDWriteBitmapRenderTarget1.](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)</span><span class="sxs-lookup"><span data-stu-id="4fa08-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="4fa08-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4fa08-110">Methods</span></span>

<span data-ttu-id="4fa08-111">La **interfaz IDWriteBitmapRenderTarget2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4fa08-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="4fa08-112">Método</span><span class="sxs-lookup"><span data-stu-id="4fa08-112">Method</span></span> | <span data-ttu-id="4fa08-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fa08-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="4fa08-114">IDWriteBitmapRenderTarget2::GetBitmapData</span><span class="sxs-lookup"><span data-stu-id="4fa08-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="4fa08-115">Recupera los datos de píxeles de un destino de representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="4fa08-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="4fa08-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fa08-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4fa08-117">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="4fa08-117">**Minimum supported client**</span></span> | <span data-ttu-id="4fa08-118">Windows 10, Project Project Project [Aplicaciones Win32]</span><span class="sxs-lookup"><span data-stu-id="4fa08-118">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="4fa08-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="4fa08-119">**Header**</span></span> | <span data-ttu-id="4fa08-120">dwrite_3.h (incluir dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="4fa08-120">dwrite_3.h (include dwrite_core.h)</span></span> |