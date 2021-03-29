---
title: Propiedad IVMFloppyDrive DriveNumber (VPCCOMInterfaces. h)
description: Recupera el índice de base cero del controlador al que está conectada la unidad de disquete.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Propiedad DriveNumber Virtual PC
- Propiedad DriveNumber Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, propiedad DriveNumber
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905320"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="58b86-106">IVMFloppyDrive::D propiedad riveNumber</span><span class="sxs-lookup"><span data-stu-id="58b86-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="58b86-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="58b86-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58b86-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58b86-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58b86-109">Recupera el índice de base cero del controlador al que está conectada la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="58b86-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="58b86-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58b86-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b86-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58b86-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="58b86-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="58b86-112">Property value</span></span>

<span data-ttu-id="58b86-113">Índice de base cero del controlador.</span><span class="sxs-lookup"><span data-stu-id="58b86-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58b86-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="58b86-114">Error codes</span></span>



| <span data-ttu-id="58b86-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="58b86-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="58b86-116">Significado</span><span class="sxs-lookup"><span data-stu-id="58b86-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="58b86-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58b86-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="58b86-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="58b86-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="58b86-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="58b86-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="58b86-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="58b86-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="58b86-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="58b86-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="58b86-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="58b86-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="58b86-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58b86-123">Requirements</span></span>



| <span data-ttu-id="58b86-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="58b86-124">Requirement</span></span> | <span data-ttu-id="58b86-125">Value</span><span class="sxs-lookup"><span data-stu-id="58b86-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b86-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58b86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58b86-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="58b86-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58b86-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58b86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58b86-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="58b86-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="58b86-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="58b86-130">End of client support</span></span><br/>    | <span data-ttu-id="58b86-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58b86-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="58b86-132">Producto</span><span class="sxs-lookup"><span data-stu-id="58b86-132">Product</span></span><br/>                  | <span data-ttu-id="58b86-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58b86-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="58b86-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58b86-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="58b86-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="58b86-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="58b86-136">IID</span><span class="sxs-lookup"><span data-stu-id="58b86-136">IID</span></span><br/>                      | <span data-ttu-id="58b86-137">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="58b86-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="58b86-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="58b86-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b86-139">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="58b86-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

