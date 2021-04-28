---
description: 'Estructura DEVICEDIALOGDATA: define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estructura DEVICEDIALOGDATA (Wiadefd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104273"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="d8fb4-103">Estructura DEVICEDIALOGDATA</span><span class="sxs-lookup"><span data-stu-id="d8fb4-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="d8fb4-104">Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8fb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8fb4-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="d8fb4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8fb4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8fb4-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-109">Especifica el tamaño de esta estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d8fb4-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-112">Especifica el identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="d8fb4-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-114">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span><span class="sxs-lookup"><span data-stu-id="d8fb4-114">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-115">Apunta a una [**interfaz IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa el elemento raíz válido en el árbol de elementos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-115">Points to an [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="d8fb4-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-118">Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="d8fb4-119">Se puede establecer en cualquiera de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d8fb4-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="d8fb4-120">Marcar</span><span class="sxs-lookup"><span data-stu-id="d8fb4-120">Flag</span></span>                                 | <span data-ttu-id="d8fb4-121">Significado</span><span class="sxs-lookup"><span data-stu-id="d8fb4-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fb4-122">0</span><span class="sxs-lookup"><span data-stu-id="d8fb4-122">0</span></span>                                    | <span data-ttu-id="d8fb4-123">Comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d8fb4-124">IMAGEN ÚNICA \_ DEL CUADRO DE DIÁLOGO DE DISPOSITIVO \_ \_ \_ WIA</span><span class="sxs-lookup"><span data-stu-id="d8fb4-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="d8fb4-125">Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo de adquisición de imágenes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="d8fb4-126">CUADRO DE DIÁLOGO \_ DE DISPOSITIVO WIA \_ USO DE LA INTERFAZ DE USUARIO \_ \_ \_ COMÚN</span><span class="sxs-lookup"><span data-stu-id="d8fb4-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="d8fb4-127">Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="d8fb4-128">Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="d8fb4-129">Si ninguna interfaz de usuario está disponible, la función devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8fb4-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-131">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-132">Especifica el tipo de datos que la imagen pretende representar.</span><span class="sxs-lookup"><span data-stu-id="d8fb4-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="d8fb4-133">Para obtener una lista de valores de intención de imagen, vea [**Constantes de intención de imagen.**](-wia-imageintentconstants.md)</span><span class="sxs-lookup"><span data-stu-id="d8fb4-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8fb4-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-135">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-136">Recibe el número de elementos de la matriz indicado por el **parámetro ppWiaItem.**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d8fb4-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="d8fb4-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="d8fb4-138">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="d8fb4-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="d8fb4-139">Recibe la dirección de una matriz de punteros a [**interfaces IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)</span><span class="sxs-lookup"><span data-stu-id="d8fb4-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8fb4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8fb4-140">Requirements</span></span>



| <span data-ttu-id="d8fb4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8fb4-141">Requirement</span></span> | <span data-ttu-id="d8fb4-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d8fb4-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fb4-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8fb4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fb4-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8fb4-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d8fb4-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8fb4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fb4-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8fb4-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d8fb4-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8fb4-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8fb4-148"><dt>Wiadefd.h</dt></span><span class="sxs-lookup"><span data-stu-id="d8fb4-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




