---
title: ImageList_SetColorTable función)
description: Establece la tabla de colores de una lista de imágenes.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable controles de función de Windows
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997192"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="f2f2d-104">ImageList \_ SetColorTable función)</span><span class="sxs-lookup"><span data-stu-id="f2f2d-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="f2f2d-105">Establece la tabla de colores de una lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2f2d-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="f2f2d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f2d-108">*himl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f2d-109">Tipo: **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="f2f2d-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="f2f2d-110">Identificador de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="f2f2d-111">*iniciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f2d-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f2f2d-112">Type: **int**</span></span>

<span data-ttu-id="f2f2d-113">Índice de tabla de colores basado en cero que especifica la primera entrada de la tabla de colores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="f2f2d-114">*longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f2d-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f2f2d-115">Type: **int**</span></span>

<span data-ttu-id="f2f2d-116">Número de entradas de la tabla de colores que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="f2f2d-117">*prgb* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f2d-118">Tipo: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="f2f2d-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="f2f2d-119">Puntero a una matriz de _len estructuras \* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que contienen información de color nueva para la tabla de colores del Dib.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f2d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f2d-120">Return value</span></span>

<span data-ttu-id="f2f2d-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="f2f2d-121">Type: **int**</span></span>

<span data-ttu-id="f2f2d-122">Si la función se ejecuta correctamente, devuelve el número de entradas de la tabla de colores establecida por la función.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="f2f2d-123">Si se produce un error en la función, el valor devuelto es menor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f2d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2f2d-124">Remarks</span></span>

<span data-ttu-id="f2f2d-125">Solo las listas de imágenes creadas con la marca [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) o [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) tienen tablas de color.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="f2f2d-126">Normalmente, la tabla de colores de una lista de imágenes se establece automáticamente copiando la tabla de colores de la primera imagen agregada a la lista (por ejemplo, a través de la función [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) si la imagen es un Dib.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="f2f2d-127">Si la primera imagen agregada a la lista de imágenes no es un DIB, la tabla de colores de la paleta de semitonos se usa para las listas de imágenes de **ILC \_ COLOR8** y la tabla de colores VGA se usa para **ILC \_ COLOR4**.</span><span class="sxs-lookup"><span data-stu-id="f2f2d-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f2d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f2d-128">Requirements</span></span>



| <span data-ttu-id="f2f2d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f2d-129">Requirement</span></span> | <span data-ttu-id="f2f2d-130">Value</span><span class="sxs-lookup"><span data-stu-id="f2f2d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f2d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f2d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f2d-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="f2f2d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f2d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f2d-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f2d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f2f2d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2f2d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2f2d-136"><dt>Comctl32.dll (versión 3,51 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f2f2d-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f2d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f2d-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2f2d-138">[Tabla de colores](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="f2f2d-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 

