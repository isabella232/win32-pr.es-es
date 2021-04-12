---
title: Propiedad de visualización IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera la presentación de vídeo de la máquina virtual.
ms.assetid: ca5a433d-4613-4b6d-9de7-d9c6a2038e38
keywords:
- Mostrar Propiedades de equipo virtual
- Propiedad display virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, Mostrar propiedad
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Display
- IVMVirtualMachine.get_Display
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175150ba76074918d497efd2c9f65a53af46b8bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491297"
---
# <a name="ivmvirtualmachinedisplay-property"></a><span data-ttu-id="d5e86-106">IVMVirtualMachine::D propiedad de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d5e86-106">IVMVirtualMachine::Display property</span></span>

<span data-ttu-id="d5e86-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5e86-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5e86-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5e86-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5e86-109">Recupera la presentación de vídeo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5e86-109">Retrieves the video display for the virtual machine.</span></span>

<span data-ttu-id="d5e86-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d5e86-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e86-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5e86-111">Syntax</span></span>


```C++
HRESULT get_Display(
  [out, retval] IVMDisplay **display
);
```



## <a name="property-value"></a><span data-ttu-id="d5e86-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d5e86-112">Property value</span></span>

<span data-ttu-id="d5e86-113">El objeto [**IVMDisplay**](ivmdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e86-113">The [**IVMDisplay**](ivmdisplay.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d5e86-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d5e86-114">Error codes</span></span>



| <span data-ttu-id="d5e86-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d5e86-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d5e86-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d5e86-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d5e86-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5e86-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d5e86-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5e86-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d5e86-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d5e86-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d5e86-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d5e86-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d5e86-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d5e86-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d5e86-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d5e86-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="d5e86-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5e86-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d5e86-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d5e86-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d5e86-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e86-125">Requirements</span></span>



| <span data-ttu-id="d5e86-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e86-126">Requirement</span></span> | <span data-ttu-id="d5e86-127">Value</span><span class="sxs-lookup"><span data-stu-id="d5e86-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e86-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e86-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e86-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5e86-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5e86-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e86-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e86-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5e86-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5e86-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d5e86-132">End of client support</span></span><br/>    | <span data-ttu-id="d5e86-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5e86-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5e86-134">Producto</span><span class="sxs-lookup"><span data-stu-id="d5e86-134">Product</span></span><br/>                  | <span data-ttu-id="d5e86-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5e86-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5e86-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5e86-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e86-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e86-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5e86-138">IID</span><span class="sxs-lookup"><span data-stu-id="d5e86-138">IID</span></span><br/>                      | <span data-ttu-id="d5e86-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d5e86-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d5e86-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e86-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e86-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d5e86-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

