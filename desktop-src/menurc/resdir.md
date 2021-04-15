---
title: Estructura RESDIR
description: Contiene información sobre un icono o componente de cursor individual de un grupo de recursos. Hay una estructura RESDIR para cada componente de grupo. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menús de la estructura RESDIR y otros recursos
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695885"
---
# <a name="resdir-structure"></a><span data-ttu-id="f2104-106">Estructura RESDIR</span><span class="sxs-lookup"><span data-stu-id="f2104-106">RESDIR structure</span></span>

<span data-ttu-id="f2104-107">Contiene información sobre un icono o componente de cursor individual de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2104-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="f2104-108">Hay una estructura **RESDIR** para cada componente de grupo.</span><span class="sxs-lookup"><span data-stu-id="f2104-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="f2104-109">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="f2104-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2104-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2104-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="f2104-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2104-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2104-112">**Icono**</span><span class="sxs-lookup"><span data-stu-id="f2104-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-113">Tipo: **[ **ICONRESDIR**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-114">El ancho, el alto y el recuento de color del icono indicado.</span><span class="sxs-lookup"><span data-stu-id="f2104-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="f2104-115">**Cursor**</span><span class="sxs-lookup"><span data-stu-id="f2104-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-116">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-117">Ancho y alto del cursor indicado.</span><span class="sxs-lookup"><span data-stu-id="f2104-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="f2104-118">**Planos**</span><span class="sxs-lookup"><span data-stu-id="f2104-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-119">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-120">Número de planos de color del mapa de bits del icono o del cursor.</span><span class="sxs-lookup"><span data-stu-id="f2104-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f2104-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="f2104-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-122">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-123">Número de bits por píxel en el mapa de bits del icono o del cursor.</span><span class="sxs-lookup"><span data-stu-id="f2104-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f2104-124">**BytesInRes**</span><span class="sxs-lookup"><span data-stu-id="f2104-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-125">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-126">Tamaño del recurso, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f2104-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f2104-127">**IconCursorId**</span><span class="sxs-lookup"><span data-stu-id="f2104-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="f2104-128">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="f2104-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2104-129">Icono o cursor con un identificador ordinal único.</span><span class="sxs-lookup"><span data-stu-id="f2104-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2104-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2104-130">Remarks</span></span>

<span data-ttu-id="f2104-131">Una o varias estructuras **RESDIR** siguen inmediatamente a la estructura [**NEWHEADER**](newheader.md) del archivo. res.</span><span class="sxs-lookup"><span data-stu-id="f2104-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="f2104-132">El miembro **ResCount** de la estructura **NEWHEADER** especifica el número de estructuras **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="f2104-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="f2104-133">Tenga en cuenta que la estructura **RESDIR** consta de una estructura [**ICONRESDIR**](iconresdir.md) o una estructura [**CURSORDIR**](cursordir.md) seguida de los miembros **aviones**, **BitCount**, **BytesInRes** y **IconCursorId** .</span><span class="sxs-lookup"><span data-stu-id="f2104-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="f2104-134">Si la estructura **RESDIR** contiene información sobre un cursor, las dos primeras **palabras** que escribe el compilador de recursos en el recurso de [ \_ cursor RT](/windows/desktop/menurc/resource-types) son los miembros **xHotSpot** y **yHotSpot** de la estructura [**LOCALHEADER**](localheader.md) .</span><span class="sxs-lookup"><span data-stu-id="f2104-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2104-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2104-135">Requirements</span></span>



| <span data-ttu-id="f2104-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2104-136">Requirement</span></span> | <span data-ttu-id="f2104-137">Value</span><span class="sxs-lookup"><span data-stu-id="f2104-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f2104-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2104-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f2104-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2104-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f2104-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2104-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f2104-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2104-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f2104-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2104-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2104-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f2104-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2104-144">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="f2104-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="f2104-145">**ICONRESDIR**</span><span class="sxs-lookup"><span data-stu-id="f2104-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="f2104-146">**LOCALHEADER**</span><span class="sxs-lookup"><span data-stu-id="f2104-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="f2104-147">**NEWHEADER**</span><span class="sxs-lookup"><span data-stu-id="f2104-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="f2104-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f2104-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2104-149">Recursos</span><span class="sxs-lookup"><span data-stu-id="f2104-149">Resources</span></span>](resources.md)
</dt> </dl>

 

