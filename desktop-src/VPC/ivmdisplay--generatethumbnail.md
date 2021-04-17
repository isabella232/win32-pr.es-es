---
title: Método _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual. | Método _GenerateThumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail método virtual PC
- Método _GenerateThumbnail Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, método _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653203"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="2a580-107">IVMDisplay:: \_ GenerateThumbnail (método)</span><span class="sxs-lookup"><span data-stu-id="2a580-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="2a580-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2a580-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a580-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a580-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a580-110">Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2a580-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a580-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a580-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="2a580-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a580-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a580-113">*thumbnailImage* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2a580-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a580-114">Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2a580-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a580-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a580-115">Return value</span></span>

<span data-ttu-id="2a580-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2a580-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2a580-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a580-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2a580-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a580-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2a580-119"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a580-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2a580-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a580-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2a580-121"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2a580-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2a580-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2a580-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2a580-123"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2a580-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2a580-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="2a580-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a580-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a580-125">Remarks</span></span>

<span data-ttu-id="2a580-126">Esta interfaz devuelve la miniatura de forma más eficaz que la propiedad [**thumbnail**](ivmdisplay-thumbnail.md) , pero no se puede usar desde los clientes de scripting.</span><span class="sxs-lookup"><span data-stu-id="2a580-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="2a580-127">La miniatura es siempre de 64 píxeles de ancho por 48 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="2a580-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="2a580-128">Cada píxel es 32 bits, donde los 8 bits superiores representan el valor azul del píxel, los 8 bits siguientes representan el valor verde del píxel y los 8 bits siguientes representan el valor rojo del píxel.</span><span class="sxs-lookup"><span data-stu-id="2a580-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="2a580-129">Los primeros 64 elementos de la matriz son la primera fila de la miniatura, los siguientes 64 elementos son la segunda fila, etc.</span><span class="sxs-lookup"><span data-stu-id="2a580-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="2a580-130">Este método devuelve una matriz estática de píxeles, que es más eficaz que devolver una **SAFEARRAY** de valores **Variant** , pero no es compatible con los clientes de scripting.</span><span class="sxs-lookup"><span data-stu-id="2a580-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a580-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a580-131">Requirements</span></span>



| <span data-ttu-id="2a580-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a580-132">Requirement</span></span> | <span data-ttu-id="2a580-133">Value</span><span class="sxs-lookup"><span data-stu-id="2a580-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a580-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a580-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2a580-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a580-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a580-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a580-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2a580-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2a580-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a580-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2a580-138">End of client support</span></span><br/>    | <span data-ttu-id="2a580-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a580-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a580-140">Producto</span><span class="sxs-lookup"><span data-stu-id="2a580-140">Product</span></span><br/>                  | <span data-ttu-id="2a580-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a580-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a580-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a580-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a580-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a580-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a580-144">IID</span><span class="sxs-lookup"><span data-stu-id="2a580-144">IID</span></span><br/>                      | <span data-ttu-id="2a580-145">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="2a580-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2a580-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a580-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a580-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="2a580-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

