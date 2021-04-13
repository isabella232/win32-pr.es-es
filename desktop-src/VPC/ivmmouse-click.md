---
title: Método click de IVMMouse (VPCCOMInterfaces. h)
description: Simula un clic del botón del mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Haga clic en método virtual PC
- Haga clic en método virtual PC, IVMMouse interfaz
- Interfaz de IVMMouse Virtual PC, haga clic en método
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492892"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="37b31-106">IVMMouse:: click (método)</span><span class="sxs-lookup"><span data-stu-id="37b31-106">IVMMouse::Click method</span></span>

<span data-ttu-id="37b31-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="37b31-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="37b31-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="37b31-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="37b31-109">Simula un clic del botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="37b31-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b31-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37b31-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="37b31-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37b31-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b31-112">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37b31-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b31-113">Índice del botón en el que se va a hacer clic.</span><span class="sxs-lookup"><span data-stu-id="37b31-113">The index of the button being clicked.</span></span> <span data-ttu-id="37b31-114">Para obtener una lista de valores, vea [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="37b31-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b31-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37b31-115">Return value</span></span>

<span data-ttu-id="37b31-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="37b31-116">This method can return one of these values.</span></span>



| <span data-ttu-id="37b31-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37b31-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="37b31-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="37b31-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37b31-119"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="37b31-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="37b31-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="37b31-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="37b31-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="37b31-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="37b31-123"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="37b31-124">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="37b31-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="37b31-125"><dt>**Máquina virtual \_ E \_ mouse \_ no \_ activo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="37b31-126">No se pudo completar la operación porque el dispositivo del mouse no está encendido o no está activo actualmente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="37b31-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="37b31-127"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="37b31-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="37b31-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="37b31-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b31-129">Requirements</span></span>



| <span data-ttu-id="37b31-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b31-130">Requirement</span></span> | <span data-ttu-id="37b31-131">Value</span><span class="sxs-lookup"><span data-stu-id="37b31-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b31-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b31-132">Minimum supported client</span></span><br/> | <span data-ttu-id="37b31-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="37b31-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37b31-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37b31-134">Minimum supported server</span></span><br/> | <span data-ttu-id="37b31-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="37b31-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="37b31-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="37b31-136">End of client support</span></span><br/>    | <span data-ttu-id="37b31-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37b31-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="37b31-138">Producto</span><span class="sxs-lookup"><span data-stu-id="37b31-138">Product</span></span><br/>                  | <span data-ttu-id="37b31-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="37b31-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="37b31-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37b31-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b31-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b31-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="37b31-142">IID</span><span class="sxs-lookup"><span data-stu-id="37b31-142">IID</span></span><br/>                      | <span data-ttu-id="37b31-143">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="37b31-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="37b31-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="37b31-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b31-145">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="37b31-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

