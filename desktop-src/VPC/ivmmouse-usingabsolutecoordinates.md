---
title: Propiedad IVMMouse UsingAbsoluteCoordinates (VPCCOMInterfaces. h)
description: Recupera si las coordenadas del mouse representan coordenadas absolutas o relativas.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Propiedad UsingAbsoluteCoordinates Virtual PC
- Propiedad UsingAbsoluteCoordinates Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, propiedad UsingAbsoluteCoordinates
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535098"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="32c9c-106">IVMMouse:: UsingAbsoluteCoordinates (propiedad)</span><span class="sxs-lookup"><span data-stu-id="32c9c-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="32c9c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="32c9c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="32c9c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="32c9c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="32c9c-109">Recupera si las coordenadas del mouse representan coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="32c9c-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="32c9c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="32c9c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c9c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32c9c-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="32c9c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="32c9c-112">Property value</span></span>

<span data-ttu-id="32c9c-113">**Variante \_ TRUE** para establecer que el dispositivo del mouse use coordenadas absolutas, **Variant \_ false** para usar coordenadas relativas.</span><span class="sxs-lookup"><span data-stu-id="32c9c-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32c9c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="32c9c-114">Error codes</span></span>



| <span data-ttu-id="32c9c-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="32c9c-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="32c9c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="32c9c-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32c9c-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="32c9c-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="32c9c-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="32c9c-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="32c9c-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="32c9c-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="32c9c-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="32c9c-122">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="32c9c-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="32c9c-123"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="32c9c-124">Los componentes de integración no están instalados.</span><span class="sxs-lookup"><span data-stu-id="32c9c-124">Integration components are not installed.</span></span> <span data-ttu-id="32c9c-125">Los componentes de integración son necesarios para utilizar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="32c9c-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="32c9c-126"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="32c9c-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="32c9c-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="32c9c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32c9c-128">Remarks</span></span>

<span data-ttu-id="32c9c-129">Esta propiedad solo es local para este objeto y tomará como valor predeterminado **Variant \_ false** para un nuevo objeto [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="32c9c-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="32c9c-130">Tenga en cuenta que los componentes de integración deben estar instalados para poder utilizar coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="32c9c-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c9c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32c9c-131">Requirements</span></span>



| <span data-ttu-id="32c9c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c9c-132">Requirement</span></span> | <span data-ttu-id="32c9c-133">Value</span><span class="sxs-lookup"><span data-stu-id="32c9c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c9c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32c9c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="32c9c-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="32c9c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32c9c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32c9c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="32c9c-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="32c9c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="32c9c-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="32c9c-138">End of client support</span></span><br/>    | <span data-ttu-id="32c9c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32c9c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="32c9c-140">Producto</span><span class="sxs-lookup"><span data-stu-id="32c9c-140">Product</span></span><br/>                  | <span data-ttu-id="32c9c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="32c9c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="32c9c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32c9c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c9c-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c9c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="32c9c-144">IID</span><span class="sxs-lookup"><span data-stu-id="32c9c-144">IID</span></span><br/>                      | <span data-ttu-id="32c9c-145">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="32c9c-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="32c9c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="32c9c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c9c-147">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="32c9c-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

