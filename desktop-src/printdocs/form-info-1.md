---
description: La estructura FORM_INFO_1 contiene información sobre un formulario de impresión. La información incluye el origen de los formularios de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Estructura de FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720592"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="00a6d-104">Estructura de FORM_INFO_1</span><span class="sxs-lookup"><span data-stu-id="00a6d-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="00a6d-105">La estructura **FORM_INFO_1** contiene información sobre un formulario de impresión.</span><span class="sxs-lookup"><span data-stu-id="00a6d-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="00a6d-106">La información incluye el origen del formulario de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.</span><span class="sxs-lookup"><span data-stu-id="00a6d-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a6d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00a6d-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="00a6d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="00a6d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00a6d-109">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="00a6d-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="00a6d-110">Propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="00a6d-110">The form properties.</span></span> <span data-ttu-id="00a6d-111">Se definen los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="00a6d-111">The following values are defined.</span></span>



| <span data-ttu-id="00a6d-112">Value</span><span class="sxs-lookup"><span data-stu-id="00a6d-112">Value</span></span>         | <span data-ttu-id="00a6d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="00a6d-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a6d-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="00a6d-114">FORM_USER</span></span>    | <span data-ttu-id="00a6d-115">Si se establece esta marca de bits, el formulario lo ha definido el usuario.</span><span class="sxs-lookup"><span data-stu-id="00a6d-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="00a6d-116">Los formularios con este marcador se definen en el registro.</span><span class="sxs-lookup"><span data-stu-id="00a6d-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="00a6d-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="00a6d-117">FORM_BUILTIN</span></span> | <span data-ttu-id="00a6d-118">Si se establece esta marca de bits, el formulario forma parte del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="00a6d-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="00a6d-119">Las definiciones de formulario con este marcador establecido no aparecen en el registro.</span><span class="sxs-lookup"><span data-stu-id="00a6d-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="00a6d-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="00a6d-120">FORM_PRINTER</span></span> | <span data-ttu-id="00a6d-121">Si se establece esta marca de bits, el formulario está asociado a una impresora determinada y su definición aparece en el registro.</span><span class="sxs-lookup"><span data-stu-id="00a6d-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="00a6d-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="00a6d-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="00a6d-123">Puntero a una cadena terminada en null que especifica el nombre del formulario.</span><span class="sxs-lookup"><span data-stu-id="00a6d-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="00a6d-124">El nombre del formulario no puede superar los 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="00a6d-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="00a6d-125">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="00a6d-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="00a6d-126">Ancho y alto, en milésimas de milímetro, del formulario.</span><span class="sxs-lookup"><span data-stu-id="00a6d-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="00a6d-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="00a6d-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="00a6d-128">Ancho y alto, en milésimas de milímetro, del formulario.</span><span class="sxs-lookup"><span data-stu-id="00a6d-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00a6d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a6d-129">Requirements</span></span>



| <span data-ttu-id="00a6d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a6d-130">Requirement</span></span> | <span data-ttu-id="00a6d-131">Value</span><span class="sxs-lookup"><span data-stu-id="00a6d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a6d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a6d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="00a6d-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00a6d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00a6d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a6d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="00a6d-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00a6d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00a6d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a6d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a6d-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00a6d-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="00a6d-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="00a6d-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="00a6d-139">**_FORM_INFO_1W** (Unicode) y **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="00a6d-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="00a6d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="00a6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a6d-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="00a6d-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="00a6d-142">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="00a6d-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="00a6d-143">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="00a6d-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="00a6d-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="00a6d-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="00a6d-145">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="00a6d-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




