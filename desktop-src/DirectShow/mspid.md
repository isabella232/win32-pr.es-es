---
description: Tenga en cuenta que esta API está en desuso. Las nuevas aplicaciones no deben utilizarla. El tipo de datos MSPID identifica el propósito de una secuencia de medios.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690736"
---
# <a name="mspid"></a><span data-ttu-id="7ab3b-105">MSPID</span><span class="sxs-lookup"><span data-stu-id="7ab3b-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="7ab3b-106">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-106">This API is deprecated.</span></span> <span data-ttu-id="7ab3b-107">Las nuevas aplicaciones no deben utilizarla.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-107">New applications should not use it.</span></span>

 

<span data-ttu-id="7ab3b-108">El tipo de datos **MSPID** identifica el propósito de una secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="7ab3b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab3b-109">Remarks</span></span>

<span data-ttu-id="7ab3b-110">**MSPID** es simplemente una definición de tipo para GUID.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="7ab3b-111">Se definen los siguientes MSPIDs.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="7ab3b-112">Value</span><span class="sxs-lookup"><span data-stu-id="7ab3b-112">Value</span></span>               | <span data-ttu-id="7ab3b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab3b-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="7ab3b-114">MSPID \_ PrimaryVideo</span><span class="sxs-lookup"><span data-stu-id="7ab3b-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="7ab3b-115">Secuencia de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-115">Primary video stream.</span></span> |
| <span data-ttu-id="7ab3b-116">MSPID \_ PrimaryAudio</span><span class="sxs-lookup"><span data-stu-id="7ab3b-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="7ab3b-117">Secuencia de audio principal.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="7ab3b-118">El tipo **REFMSPID** define una referencia a un **MSPID**.</span><span class="sxs-lookup"><span data-stu-id="7ab3b-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab3b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ab3b-119">Requirements</span></span>



| <span data-ttu-id="7ab3b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab3b-120">Requirement</span></span> | <span data-ttu-id="7ab3b-121">Value</span><span class="sxs-lookup"><span data-stu-id="7ab3b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab3b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ab3b-122">Header</span></span><br/> | <dl> <span data-ttu-id="7ab3b-123"><dt>Mmstream. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab3b-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab3b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ab3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab3b-125">Tipos de datos de transmisión por secuencias multimedia</span><span class="sxs-lookup"><span data-stu-id="7ab3b-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




