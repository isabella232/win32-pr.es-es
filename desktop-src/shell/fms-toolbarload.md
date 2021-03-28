---
description: Contiene información acerca de los botones personalizados que se van a agregar a la barra de herramientas del administrador de archivos. Los botones los proporciona un archivo DLL de extensión del administrador de archivos.
title: FMS_TOOLBARLOAD estructura (Wfext. h)
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
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985507"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="b7af2-104">Estructura de FMS \_ TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="b7af2-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="b7af2-105">Contiene información acerca de los botones personalizados que se van a agregar a la barra de herramientas del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7af2-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="b7af2-106">Los botones los proporciona un archivo DLL de extensión del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7af2-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7af2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7af2-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="b7af2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7af2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7af2-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="b7af2-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b7af2-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-111">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b7af2-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="b7af2-112">El administrador de archivos establece el tamaño antes de llamar a la extensión y comprueba el tamaño después de que el procedimiento de extensión se devuelva.</span><span class="sxs-lookup"><span data-stu-id="b7af2-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="b7af2-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="b7af2-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-114">Escriba: **\_ botón LPEXT**</span><span class="sxs-lookup"><span data-stu-id="b7af2-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-115">Dirección de una matriz de estructuras [**de \_ botones ext**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="b7af2-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="b7af2-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="b7af2-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b7af2-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-118">El número de estructuras de [**\_ botón ext**](ext-button.md) en la matriz a la que señala el miembro **lpButtons** .</span><span class="sxs-lookup"><span data-stu-id="b7af2-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="b7af2-119">Este número es igual al número de botones y separadores que se van a agregar a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b7af2-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="b7af2-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="b7af2-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-121">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b7af2-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-122">Número de botones que representa el mapa de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="b7af2-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b7af2-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7af2-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b7af2-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-125">Identificador de un recurso de mapa de bits en el archivo ejecutable para el archivo DLL de extensión.</span><span class="sxs-lookup"><span data-stu-id="b7af2-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="b7af2-126">El recurso de mapa de bits contiene imágenes para el número de botones especificado por **cBitmaps**.</span><span class="sxs-lookup"><span data-stu-id="b7af2-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="b7af2-127">El administrador de archivos carga el recurso de mapa de bits y, a continuación, lo usa para mostrar los botones.</span><span class="sxs-lookup"><span data-stu-id="b7af2-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="b7af2-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7af2-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b7af2-129">Tipo: **hBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7af2-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="b7af2-130">Identificador de un mapa de bits que el administrador de archivos usará para obtener y mostrar imágenes de botón si **idBitmap** es 0.</span><span class="sxs-lookup"><span data-stu-id="b7af2-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7af2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7af2-131">Requirements</span></span>



| <span data-ttu-id="b7af2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7af2-132">Requirement</span></span> | <span data-ttu-id="b7af2-133">Value</span><span class="sxs-lookup"><span data-stu-id="b7af2-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7af2-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7af2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b7af2-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b7af2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b7af2-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7af2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b7af2-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7af2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7af2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7af2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7af2-139"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7af2-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7af2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7af2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7af2-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="b7af2-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




