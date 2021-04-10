---
description: Representa una descripción de un formato de textura.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixEngineTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997889"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="8f1da-103"><span id="vspixengine.pixenginetextureformatdesc"></span>Estructura PixEngineTextureFormatDesc</span><span class="sxs-lookup"><span data-stu-id="8f1da-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="8f1da-104">Representa una descripción de un formato de textura.</span><span class="sxs-lookup"><span data-stu-id="8f1da-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f1da-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="8f1da-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f1da-106">Members</span></span>

<span data-ttu-id="8f1da-107">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="8f1da-107">**dxgiFormat**</span></span>  
<span data-ttu-id="8f1da-108">Formato de DXGI de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f1da-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="8f1da-109">**dataFormat**</span><span class="sxs-lookup"><span data-stu-id="8f1da-109">**dataFormat**</span></span>  
<span data-ttu-id="8f1da-110">Formato de datos de la textura.</span><span class="sxs-lookup"><span data-stu-id="8f1da-110">The data format of the texture.</span></span>

<span data-ttu-id="8f1da-111">**blockBytes**</span><span class="sxs-lookup"><span data-stu-id="8f1da-111">**blockBytes**</span></span>  
<span data-ttu-id="8f1da-112">El número de bytes en un bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="8f1da-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="8f1da-113">**blockHeight**</span><span class="sxs-lookup"><span data-stu-id="8f1da-113">**blockHeight**</span></span>  
<span data-ttu-id="8f1da-114">El alto (número de muestras en el eje Y) del bloque.</span><span class="sxs-lookup"><span data-stu-id="8f1da-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="8f1da-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="8f1da-115">**blockWidth**</span></span>  
<span data-ttu-id="8f1da-116">El ancho (número de muestras en el eje X) del bloque.</span><span class="sxs-lookup"><span data-stu-id="8f1da-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="8f1da-117">**channelX**</span><span class="sxs-lookup"><span data-stu-id="8f1da-117">**channelX**</span></span>  
<span data-ttu-id="8f1da-118">Describe las propiedades del canal X.</span><span class="sxs-lookup"><span data-stu-id="8f1da-118">Describes properties of the X channel.</span></span> <span data-ttu-id="8f1da-119">Para obtener más información, vea la estructura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="8f1da-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="8f1da-120">**canaly**</span><span class="sxs-lookup"><span data-stu-id="8f1da-120">**channelY**</span></span>  
<span data-ttu-id="8f1da-121">Describe las propiedades del canal Y.</span><span class="sxs-lookup"><span data-stu-id="8f1da-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="8f1da-122">Para obtener más información, vea la estructura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="8f1da-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="8f1da-123">**channelZ**</span><span class="sxs-lookup"><span data-stu-id="8f1da-123">**channelZ**</span></span>  
<span data-ttu-id="8f1da-124">Describe las propiedades del canal Z.</span><span class="sxs-lookup"><span data-stu-id="8f1da-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="8f1da-125">Para obtener más información, vea la estructura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="8f1da-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="8f1da-126">**channelW**</span><span class="sxs-lookup"><span data-stu-id="8f1da-126">**channelW**</span></span>  
<span data-ttu-id="8f1da-127">Describe las propiedades del canal W.</span><span class="sxs-lookup"><span data-stu-id="8f1da-127">Describes properties of the W channel.</span></span> <span data-ttu-id="8f1da-128">Para obtener más información, vea la estructura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="8f1da-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="8f1da-129">**swizzle**</span><span class="sxs-lookup"><span data-stu-id="8f1da-129">**swizzle**</span></span>  
<span data-ttu-id="8f1da-130">Describe la swizzle (intercambio de canales) aplicada al ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8f1da-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f1da-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f1da-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8f1da-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f1da-132">Header</span></span></p></td><td><span data-ttu-id="8f1da-133">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8f1da-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



