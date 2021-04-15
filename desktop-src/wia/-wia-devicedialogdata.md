---
description: Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estructura DEVICEDIALOGDATA (Wiadefd. h)
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
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545566"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="a6966-103">Estructura DEVICEDIALOGDATA</span><span class="sxs-lookup"><span data-stu-id="a6966-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="a6966-104">Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6966-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6966-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6966-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a6966-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6966-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6966-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a6966-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6966-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6966-109">Especifica el tamaño de esta estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="a6966-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a6966-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="a6966-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-111">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="a6966-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="a6966-112">Especifica el identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a6966-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="a6966-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="a6966-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-114">Tipo: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="a6966-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="a6966-115">Apunta a una interfaz [_ *IWiaItem* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa el elemento raíz válido en el árbol de elementos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6966-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="a6966-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="a6966-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6966-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6966-118">Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a6966-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="a6966-119">Se puede establecer en cualquiera de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a6966-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="a6966-120">Marca</span><span class="sxs-lookup"><span data-stu-id="a6966-120">Flag</span></span>                                 | <span data-ttu-id="a6966-121">Significado</span><span class="sxs-lookup"><span data-stu-id="a6966-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6966-122">0</span><span class="sxs-lookup"><span data-stu-id="a6966-122">0</span></span>                                    | <span data-ttu-id="a6966-123">Comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6966-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="a6966-124">\_cuadro de diálogo de dispositivo WIA \_ \_ \_ imagen única</span><span class="sxs-lookup"><span data-stu-id="a6966-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="a6966-125">Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo adquisición de imagen de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6966-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="a6966-126">cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común</span><span class="sxs-lookup"><span data-stu-id="a6966-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="a6966-127">Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a6966-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="a6966-128">Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a6966-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="a6966-129">Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a6966-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a6966-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="a6966-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-131">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="a6966-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="a6966-132">Especifica el tipo de datos que va a representar la imagen.</span><span class="sxs-lookup"><span data-stu-id="a6966-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="a6966-133">Para obtener una lista de valores de intención de imagen, vea [**constantes de intención de imagen**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="a6966-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6966-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="a6966-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-135">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="a6966-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="a6966-136">Recibe el número de elementos de la matriz indicado por el parámetro **ppWiaItem** .</span><span class="sxs-lookup"><span data-stu-id="a6966-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a6966-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="a6966-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="a6966-138">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6966-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="a6966-139">Recibe la dirección de una matriz de punteros a las interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="a6966-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6966-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6966-140">Requirements</span></span>



| <span data-ttu-id="a6966-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6966-141">Requirement</span></span> | <span data-ttu-id="a6966-142">Value</span><span class="sxs-lookup"><span data-stu-id="a6966-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6966-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6966-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a6966-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6966-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6966-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6966-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a6966-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6966-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6966-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6966-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6966-148"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6966-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




