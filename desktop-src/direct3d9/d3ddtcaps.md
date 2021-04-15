---
description: Constantes que describen los tipos de datos de vértices admitidos por un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696114"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="d855c-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="d855c-103">D3DDTCAPS</span></span>

<span data-ttu-id="d855c-104">Constantes que describen los tipos de datos de vértices admitidos por un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d855c-104">Constants describing the vertex data types supported by a device.</span></span>



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d855c-105">\#define</span><span class="sxs-lookup"><span data-stu-id="d855c-105">\#define</span></span>              | <span data-ttu-id="d855c-106">Value</span><span class="sxs-lookup"><span data-stu-id="d855c-106">Value</span></span>       | <span data-ttu-id="d855c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d855c-107">Description</span></span>                                                                                                                   |
| <span data-ttu-id="d855c-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d855c-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="d855c-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="d855c-109">0x00000001L</span></span> | <span data-ttu-id="d855c-110">4D sin signo.</span><span class="sxs-lookup"><span data-stu-id="d855c-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="d855c-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="d855c-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="d855c-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="d855c-112">0x00000002L</span></span> | <span data-ttu-id="d855c-113">Byte sin signo normalizado y 4D.</span><span class="sxs-lookup"><span data-stu-id="d855c-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="d855c-114">Cada uno de los cuatro bytes se normaliza dividiendo en 255,0.</span><span class="sxs-lookup"><span data-stu-id="d855c-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="d855c-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="d855c-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="d855c-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="d855c-116">0x00000004L</span></span> | <span data-ttu-id="d855c-117">Normalizado, 2D con signo corto, expandido a (primer byte/32767.0, segundo byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="d855c-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="d855c-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="d855c-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="d855c-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="d855c-119">0x00000008L</span></span> | <span data-ttu-id="d855c-120">Normalizado, 4D con signo corto, expandido a (primer byte/32767.0, segundo byte/32767.0, tercer byte/32767.0, cuarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="d855c-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="d855c-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="d855c-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="d855c-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="d855c-122">0x00000010L</span></span> | <span data-ttu-id="d855c-123">Normalizado, 2D sin signo corto, expandido a (primer byte/65535.0, segundo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="d855c-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="d855c-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="d855c-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="d855c-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="d855c-125">0x00000020L</span></span> | <span data-ttu-id="d855c-126">4D normalizado sin signo, expandido a (primer byte/65535.0, segundo byte/65535.0, tercer byte/65535.0, cuarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="d855c-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="d855c-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="d855c-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="d855c-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="d855c-128">0x00000040L</span></span> | <span data-ttu-id="d855c-129">formato 3D sin signo 10 10 10 expandido a (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="d855c-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="d855c-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="d855c-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="d855c-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="d855c-131">0x00000080L</span></span> | <span data-ttu-id="d855c-132">formato 3D con signo 10 10 10 normalizado y expandido a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="d855c-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="d855c-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="d855c-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="d855c-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="d855c-134">0x00000100L</span></span> | <span data-ttu-id="d855c-135">números de punto flotante de 16 bits 2D.</span><span class="sxs-lookup"><span data-stu-id="d855c-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="d855c-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d855c-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="d855c-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="d855c-137">0x00000200L</span></span> | <span data-ttu-id="d855c-138">4D números de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d855c-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="d855c-139">El miembro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="d855c-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d855c-140">Información constante</span><span class="sxs-lookup"><span data-stu-id="d855c-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d855c-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d855c-141">Header</span></span>                   | <span data-ttu-id="d855c-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d855c-142">d3d9caps.h</span></span> |
| <span data-ttu-id="d855c-143">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="d855c-143">Minimum operating system</span></span> | <span data-ttu-id="d855c-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d855c-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d855c-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d855c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d855c-146">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d855c-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



