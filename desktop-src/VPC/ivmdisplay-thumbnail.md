---
title: Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces. h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Propiedad IVMDisplay Thumbnail (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propiedad thumbnail Virtual PC
- Propiedad thumbnail Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003499"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="dd332-107">IVMDisplay:: Thumbnail (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dd332-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="dd332-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd332-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd332-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd332-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd332-110">Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd332-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="dd332-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd332-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd332-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd332-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="dd332-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dd332-113">Property value</span></span>

<span data-ttu-id="dd332-114">Una variante de tipo VT de \_ matriz VT \| \_ que contiene entradas de tipo VT \_ UI4, una para cada píxel de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="dd332-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd332-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="dd332-115">Error codes</span></span>



| <span data-ttu-id="dd332-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="dd332-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dd332-117">Significado</span><span class="sxs-lookup"><span data-stu-id="dd332-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dd332-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd332-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dd332-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd332-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="dd332-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dd332-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dd332-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="dd332-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="dd332-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dd332-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dd332-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="dd332-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dd332-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd332-124">Remarks</span></span>

<span data-ttu-id="dd332-125">Esta interfaz devuelve la miniatura menos eficaz que el método [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , pero se puede usar desde los clientes de scripting.</span><span class="sxs-lookup"><span data-stu-id="dd332-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="dd332-126">La miniatura es siempre de 64 píxeles de ancho por 48 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="dd332-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="dd332-127">Cada píxel es 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd332-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="dd332-128">Los primeros 64 elementos de la matriz son la primera fila de píxeles de la miniatura, los siguientes 64 elementos son la segunda fila, etc.</span><span class="sxs-lookup"><span data-stu-id="dd332-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd332-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd332-129">Requirements</span></span>



| <span data-ttu-id="dd332-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd332-130">Requirement</span></span> | <span data-ttu-id="dd332-131">Value</span><span class="sxs-lookup"><span data-stu-id="dd332-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd332-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd332-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dd332-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd332-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd332-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd332-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dd332-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dd332-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd332-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dd332-136">End of client support</span></span><br/>    | <span data-ttu-id="dd332-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd332-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd332-138">Producto</span><span class="sxs-lookup"><span data-stu-id="dd332-138">Product</span></span><br/>                  | <span data-ttu-id="dd332-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd332-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd332-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd332-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd332-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd332-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dd332-142">IID</span><span class="sxs-lookup"><span data-stu-id="dd332-142">IID</span></span><br/>                      | <span data-ttu-id="dd332-143">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="dd332-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="dd332-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd332-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd332-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="dd332-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

