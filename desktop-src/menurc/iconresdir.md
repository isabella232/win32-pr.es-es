---
title: Estructura ICONRESDIR
description: Contiene las dimensiones y el formato de color de una imagen de icono individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menús de la estructura ICONRESDIR y otros recursos
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666019"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="c118c-105">Estructura ICONRESDIR</span><span class="sxs-lookup"><span data-stu-id="c118c-105">ICONRESDIR structure</span></span>

<span data-ttu-id="c118c-106">Contiene las dimensiones y el formato de color de una imagen de icono individual de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c118c-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="c118c-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="c118c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c118c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c118c-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="c118c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c118c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c118c-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="c118c-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c118c-111">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="c118c-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c118c-112">Ancho del icono, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c118c-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="c118c-113">Los valores aceptables son 16, 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="c118c-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="c118c-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="c118c-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c118c-115">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="c118c-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c118c-116">Alto del icono, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c118c-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="c118c-117">Los valores aceptables son 16, 32 y 64.</span><span class="sxs-lookup"><span data-stu-id="c118c-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="c118c-118">**ColorCount**</span><span class="sxs-lookup"><span data-stu-id="c118c-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="c118c-119">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="c118c-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c118c-120">El número de colores en el icono.</span><span class="sxs-lookup"><span data-stu-id="c118c-120">The number of colors in the icon.</span></span> <span data-ttu-id="c118c-121">Los valores aceptables son 2, 8 y 16.</span><span class="sxs-lookup"><span data-stu-id="c118c-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="c118c-122">**sector**</span><span class="sxs-lookup"><span data-stu-id="c118c-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c118c-123">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="c118c-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c118c-124">Sector debe establecerse en el mismo valor que el del campo reservado en el encabezado del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="c118c-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c118c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c118c-125">Remarks</span></span>

<span data-ttu-id="c118c-126">La estructura **ICONRESDIR** se pasa en la estructura [**RESDIR**](resdir.md) si la estructura **RESDIR** describe un icono.</span><span class="sxs-lookup"><span data-stu-id="c118c-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="c118c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c118c-127">Requirements</span></span>



| <span data-ttu-id="c118c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c118c-128">Requirement</span></span> | <span data-ttu-id="c118c-129">Value</span><span class="sxs-lookup"><span data-stu-id="c118c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c118c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c118c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c118c-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c118c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c118c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c118c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c118c-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c118c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c118c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c118c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c118c-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c118c-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c118c-136">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="c118c-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="c118c-137">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c118c-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c118c-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="c118c-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





