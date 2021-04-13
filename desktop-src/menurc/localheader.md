---
title: Estructura LOCALHEADER
description: Contiene las coordenadas x e y de una zona activa asociada al cursor identificado por una estructura RESDIR. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menús de la estructura LOCALHEADER y otros recursos
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422408"
---
# <a name="localheader-structure"></a><span data-ttu-id="8c55c-105">Estructura LOCALHEADER</span><span class="sxs-lookup"><span data-stu-id="8c55c-105">LOCALHEADER structure</span></span>

<span data-ttu-id="8c55c-106">Contiene las coordenadas x e y de una zona activa asociada al cursor identificado por una estructura [**RESDIR**](resdir.md) .</span><span class="sxs-lookup"><span data-stu-id="8c55c-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="8c55c-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="8c55c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c55c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c55c-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="8c55c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c55c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c55c-110">**xHotSpot**</span><span class="sxs-lookup"><span data-stu-id="8c55c-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="8c55c-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="8c55c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8c55c-112">Coordenada x de la zona activa del cursor, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="8c55c-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8c55c-113">**yHotSpot**</span><span class="sxs-lookup"><span data-stu-id="8c55c-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="8c55c-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="8c55c-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8c55c-115">Coordenada y de la zona activa del cursor, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="8c55c-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c55c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c55c-116">Remarks</span></span>

<span data-ttu-id="8c55c-117">La estructura **LOCALHEADER** es la primera de los datos que se escriben en el recurso de [ \_ cursor RT](/windows/desktop/menurc/resource-types) si una estructura [**RESDIR**](resdir.md) contiene información sobre un cursor.</span><span class="sxs-lookup"><span data-stu-id="8c55c-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c55c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c55c-118">Requirements</span></span>



| <span data-ttu-id="8c55c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c55c-119">Requirement</span></span> | <span data-ttu-id="8c55c-120">Value</span><span class="sxs-lookup"><span data-stu-id="8c55c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8c55c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c55c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c55c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c55c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c55c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c55c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c55c-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c55c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8c55c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c55c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c55c-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8c55c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c55c-127">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="8c55c-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="8c55c-128">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="8c55c-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="8c55c-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8c55c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c55c-130">Recursos</span><span class="sxs-lookup"><span data-stu-id="8c55c-130">Resources</span></span>](resources.md)
</dt> </dl>

 

