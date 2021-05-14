---
description: Contiene información sobre los botones personalizados que se van a agregar a la barra de herramientas del Administrador de archivos. Los botones los proporciona un archivo DLL de extensión del Administrador de archivos.
title: FMS_TOOLBARLOAD estructura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842166"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="670e7-104">ESTRUCTURA FMS \_ TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="670e7-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="670e7-105">Contiene información sobre los botones personalizados que se van a agregar a la barra de herramientas del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="670e7-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="670e7-106">Los botones los proporciona un archivo DLL de extensión del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="670e7-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="670e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="670e7-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="670e7-108">Members</span><span class="sxs-lookup"><span data-stu-id="670e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="670e7-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="670e7-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="670e7-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-111">Tamaño, en bytes, de la estructura .</span><span class="sxs-lookup"><span data-stu-id="670e7-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="670e7-112">El Administrador de archivos establece el tamaño antes de llamar a la extensión y comprueba el tamaño después de que se devuelva el procedimiento de extensión.</span><span class="sxs-lookup"><span data-stu-id="670e7-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="670e7-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="670e7-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-114">Tipo: **LPEXT \_ BUTTON**</span><span class="sxs-lookup"><span data-stu-id="670e7-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-115">Dirección de una matriz de [**estructuras EXT \_ BUTTON.**](ext-button.md)</span><span class="sxs-lookup"><span data-stu-id="670e7-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="670e7-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="670e7-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-117">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="670e7-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-118">Número de estructuras [**EXT \_ BUTTON**](ext-button.md) de la matriz a la que apunta **el miembro lpButtons.**</span><span class="sxs-lookup"><span data-stu-id="670e7-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="670e7-119">Este número es igual al número de botones y separadores que se agregarán a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="670e7-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="670e7-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="670e7-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-121">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="670e7-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-122">Número de botones representados por el mapa de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="670e7-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="670e7-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="670e7-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-124">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="670e7-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-125">Identificador de un recurso de mapa de bits en el archivo ejecutable para el archivo DLL de extensión.</span><span class="sxs-lookup"><span data-stu-id="670e7-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="670e7-126">El recurso de mapa de bits contiene imágenes para el número de botones especificado por **cBitmaps.**</span><span class="sxs-lookup"><span data-stu-id="670e7-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="670e7-127">El Administrador de archivos carga el recurso de mapa de bits y, a continuación, lo usa para mostrar los botones.</span><span class="sxs-lookup"><span data-stu-id="670e7-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="670e7-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="670e7-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="670e7-129">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="670e7-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="670e7-130">Identificador de un mapa de bits que el Administrador de archivos usará para obtener y mostrar imágenes de botón si **idBitmap** es 0.</span><span class="sxs-lookup"><span data-stu-id="670e7-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="670e7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670e7-131">Requirements</span></span>



| <span data-ttu-id="670e7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="670e7-132">Requirement</span></span> | <span data-ttu-id="670e7-133">Value</span><span class="sxs-lookup"><span data-stu-id="670e7-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="670e7-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="670e7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="670e7-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="670e7-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="670e7-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="670e7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="670e7-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="670e7-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="670e7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="670e7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="670e7-139"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="670e7-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670e7-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="670e7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670e7-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="670e7-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




