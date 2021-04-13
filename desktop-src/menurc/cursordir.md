---
title: Estructura CURSORDIR
description: Contiene las dimensiones de una imagen de cursor individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menús de la estructura CURSORDIR y otros recursos
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422547"
---
# <a name="cursordir-structure"></a><span data-ttu-id="f522b-105">Estructura CURSORDIR</span><span class="sxs-lookup"><span data-stu-id="f522b-105">CURSORDIR structure</span></span>

<span data-ttu-id="f522b-106">Contiene las dimensiones de una imagen de cursor individual de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f522b-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="f522b-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="f522b-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f522b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f522b-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="f522b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f522b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f522b-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="f522b-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="f522b-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f522b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f522b-112">Ancho del cursor, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f522b-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="f522b-113">Los valores aceptables son 16, 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="f522b-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="f522b-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="f522b-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="f522b-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f522b-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f522b-116">Alto del cursor, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f522b-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="f522b-117">Los valores aceptables son 16, 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="f522b-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f522b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f522b-118">Remarks</span></span>

<span data-ttu-id="f522b-119">La estructura **CURSORDIR** se pasa en la estructura [**RESDIR**](resdir.md) si la estructura **RESDIR** describe un cursor.</span><span class="sxs-lookup"><span data-stu-id="f522b-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f522b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f522b-120">Requirements</span></span>



| <span data-ttu-id="f522b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f522b-121">Requirement</span></span> | <span data-ttu-id="f522b-122">Value</span><span class="sxs-lookup"><span data-stu-id="f522b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f522b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f522b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f522b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f522b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f522b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f522b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f522b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f522b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f522b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f522b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f522b-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f522b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f522b-129">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="f522b-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="f522b-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f522b-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f522b-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="f522b-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





