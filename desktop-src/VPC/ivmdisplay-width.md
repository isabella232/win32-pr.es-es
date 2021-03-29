---
title: Propiedad ancho IVMDisplay (VPCCOMInterfaces. h)
description: Ancho de la pantalla de la máquina virtual, en píxeles.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Propiedad width de Virtual PC
- Propiedad Width Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535188"
---
# <a name="ivmdisplaywidth-property"></a><span data-ttu-id="3c920-106">IVMDisplay:: width (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3c920-106">IVMDisplay::Width property</span></span>

<span data-ttu-id="3c920-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c920-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3c920-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3c920-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3c920-109">Recupera el ancho de la pantalla (VM) de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c920-109">Retrieves the width of the virtual machine's (VM's) display, in pixels.</span></span>

<span data-ttu-id="3c920-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3c920-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c920-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c920-111">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a><span data-ttu-id="3c920-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c920-112">Property value</span></span>

<span data-ttu-id="3c920-113">Ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c920-113">The width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c920-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3c920-114">Error codes</span></span>



| <span data-ttu-id="3c920-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3c920-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="3c920-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3c920-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c920-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="3c920-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3c920-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3c920-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="3c920-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="3c920-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c920-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="3c920-122">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="3c920-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="3c920-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3c920-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="3c920-124">La máquina virtual no es válida o no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3c920-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="3c920-125"><dt>Máquina virtual \_ E \_ no \_ Mostrar</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="3c920-126">No se puede encontrar una pantalla válida para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3c920-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="3c920-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="3c920-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3c920-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="3c920-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c920-129">Requirements</span></span>



| <span data-ttu-id="3c920-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c920-130">Requirement</span></span> | <span data-ttu-id="3c920-131">Value</span><span class="sxs-lookup"><span data-stu-id="3c920-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c920-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c920-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3c920-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c920-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c920-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c920-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3c920-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3c920-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3c920-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3c920-136">End of client support</span></span><br/>    | <span data-ttu-id="3c920-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c920-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3c920-138">Producto</span><span class="sxs-lookup"><span data-stu-id="3c920-138">Product</span></span><br/>                  | <span data-ttu-id="3c920-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3c920-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3c920-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c920-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c920-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c920-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3c920-142">IID</span><span class="sxs-lookup"><span data-stu-id="3c920-142">IID</span></span><br/>                      | <span data-ttu-id="3c920-143">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="3c920-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3c920-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c920-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c920-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="3c920-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

