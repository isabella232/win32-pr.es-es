---
description: Especifica qué bytes se cifran en una superficie de vídeo protegida.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153646"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="7602b-103">D3DENCRYPTED \_ estructura de información de bloque \_</span><span class="sxs-lookup"><span data-stu-id="7602b-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="7602b-104">Especifica qué bytes se cifran en una superficie de vídeo protegida.</span><span class="sxs-lookup"><span data-stu-id="7602b-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7602b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7602b-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="7602b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7602b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7602b-107">**NumEncryptedBytesAtBeginning**</span><span class="sxs-lookup"><span data-stu-id="7602b-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="7602b-108">Número de bytes que se cifran al principio del búfer.</span><span class="sxs-lookup"><span data-stu-id="7602b-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7602b-109">**NumBytesInSkipPattern**</span><span class="sxs-lookup"><span data-stu-id="7602b-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="7602b-110">Número de bytes que se omiten después de los primeros **NumEncryptedBytesAtBeginning** bytes y después de cada bloque de **NumBytesInEncryptPattern** bytes.</span><span class="sxs-lookup"><span data-stu-id="7602b-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="7602b-111">Los bytes omitidos no se cifran.</span><span class="sxs-lookup"><span data-stu-id="7602b-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="7602b-112">**NumBytesInEncryptPattern**</span><span class="sxs-lookup"><span data-stu-id="7602b-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="7602b-113">Número de bytes que se cifran después de cada bloque de bytes omitidos.</span><span class="sxs-lookup"><span data-stu-id="7602b-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7602b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7602b-114">Requirements</span></span>



| <span data-ttu-id="7602b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7602b-115">Requirement</span></span> | <span data-ttu-id="7602b-116">Value</span><span class="sxs-lookup"><span data-stu-id="7602b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7602b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7602b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7602b-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7602b-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7602b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7602b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7602b-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7602b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7602b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7602b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7602b-122"><dt>D3d9types. h (incluye d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7602b-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7602b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7602b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7602b-124">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7602b-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




