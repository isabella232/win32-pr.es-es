---
description: Constantes que describen los tipos de datos de vértice admitidos por un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343249"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="530a5-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="530a5-103">D3DDTCAPS</span></span>

<span data-ttu-id="530a5-104">Constantes que describen los tipos de datos de vértice admitidos por un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="530a5-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="530a5-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="530a5-105">\#define</span></span>              | <span data-ttu-id="530a5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="530a5-106">Value</span></span>       | <span data-ttu-id="530a5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="530a5-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530a5-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="530a5-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="530a5-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="530a5-109">0x00000001L</span></span> | <span data-ttu-id="530a5-110">Byte 4D sin signo.</span><span class="sxs-lookup"><span data-stu-id="530a5-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="530a5-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="530a5-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="530a5-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="530a5-112">0x00000002L</span></span> | <span data-ttu-id="530a5-113">Byte 4D sin signo normalizado.</span><span class="sxs-lookup"><span data-stu-id="530a5-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="530a5-114">Cada uno de los cuatro bytes se normaliza dividiendo a 255,0.</span><span class="sxs-lookup"><span data-stu-id="530a5-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="530a5-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="530a5-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="530a5-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="530a5-116">0x00000004L</span></span> | <span data-ttu-id="530a5-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="530a5-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="530a5-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="530a5-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="530a5-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="530a5-119">0x00000008L</span></span> | <span data-ttu-id="530a5-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="530a5-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="530a5-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="530a5-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="530a5-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="530a5-122">0x00000010L</span></span> | <span data-ttu-id="530a5-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="530a5-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="530a5-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="530a5-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="530a5-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="530a5-125">0x00000020L</span></span> | <span data-ttu-id="530a5-126">4D normalizado sin signo corto, expandido a (primer byte/65535,0, segundo byte/65535,0, tercer byte/65535,0, cuarto byte/65535,0).</span><span class="sxs-lookup"><span data-stu-id="530a5-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="530a5-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="530a5-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="530a5-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="530a5-128">0x00000040L</span></span> | <span data-ttu-id="530a5-129">Formato 3D sin signo 10 10 10 expandido a (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="530a5-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="530a5-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="530a5-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="530a5-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="530a5-131">0x00000080L</span></span> | <span data-ttu-id="530a5-132">Formato 10 10 10 con firma 3D normalizado y expandido a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="530a5-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="530a5-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="530a5-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="530a5-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="530a5-134">0x00000100L</span></span> | <span data-ttu-id="530a5-135">Números de punto flotante 2D de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="530a5-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="530a5-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="530a5-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="530a5-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="530a5-137">0x00000200L</span></span> | <span data-ttu-id="530a5-138">Números de punto flotante 4D de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="530a5-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="530a5-139">El miembro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="530a5-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="530a5-140">Información constante</span><span class="sxs-lookup"><span data-stu-id="530a5-140">Constant Information</span></span>



|  <span data-ttu-id="530a5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="530a5-141">Requirement</span></span>                        | <span data-ttu-id="530a5-142">Value</span><span class="sxs-lookup"><span data-stu-id="530a5-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="530a5-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="530a5-143">Header</span></span>                   | <span data-ttu-id="530a5-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="530a5-144">d3d9caps.h</span></span> |
| <span data-ttu-id="530a5-145">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="530a5-145">Minimum operating system</span></span> | <span data-ttu-id="530a5-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="530a5-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="530a5-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="530a5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="530a5-148">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="530a5-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



