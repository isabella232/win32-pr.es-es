---
title: Propiedad de alto IVMDisplay (VPCCOMInterfaces. h)
description: Alto de la pantalla de la máquina virtual, en píxeles.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Propiedad de alto equipo virtual PC
- Propiedad height Virtual PC, interfaz IVMDisplay
- Interfaz IVMDisplay Virtual PC, propiedad height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079444"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="c799e-106">IVMDisplay:: Height (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c799e-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="c799e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c799e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c799e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c799e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c799e-109">Recupera el alto de la pantalla de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c799e-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="c799e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c799e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c799e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c799e-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="c799e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c799e-112">Property value</span></span>

<span data-ttu-id="c799e-113">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c799e-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c799e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c799e-114">Error codes</span></span>



| <span data-ttu-id="c799e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="c799e-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="c799e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c799e-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c799e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="c799e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c799e-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c799e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="c799e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="c799e-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c799e-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="c799e-122">La máquina virtual debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="c799e-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="c799e-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c799e-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="c799e-124">La máquina virtual no es válida o no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="c799e-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="c799e-125"><dt>Máquina virtual \_ E \_ no \_ Mostrar</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="c799e-126">No se puede encontrar una pantalla válida para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c799e-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="c799e-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="c799e-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c799e-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="c799e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c799e-129">Requirements</span></span>



| <span data-ttu-id="c799e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c799e-130">Requirement</span></span> | <span data-ttu-id="c799e-131">Value</span><span class="sxs-lookup"><span data-stu-id="c799e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c799e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c799e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c799e-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c799e-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c799e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c799e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c799e-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c799e-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c799e-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c799e-136">End of client support</span></span><br/>    | <span data-ttu-id="c799e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c799e-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c799e-138">Producto</span><span class="sxs-lookup"><span data-stu-id="c799e-138">Product</span></span><br/>                  | <span data-ttu-id="c799e-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c799e-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c799e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c799e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c799e-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c799e-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c799e-142">IID</span><span class="sxs-lookup"><span data-stu-id="c799e-142">IID</span></span><br/>                      | <span data-ttu-id="c799e-143">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="c799e-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c799e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c799e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c799e-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="c799e-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

