---
title: Propiedad IVMVirtualMachine RdpPipeName (VPCCOMInterfaces. h)
description: Recupera el nombre de la canalización con nombre de la conexión RDP utilizada para el vídeo y la entrada.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Propiedad RdpPipeName Virtual PC
- Propiedad RdpPipeName Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078807"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="fbf72-106">IVMVirtualMachine:: RdpPipeName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fbf72-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="fbf72-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fbf72-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fbf72-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fbf72-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fbf72-109">Recupera el nombre de la canalización con nombre de la conexión RDP utilizada para el vídeo y la entrada.</span><span class="sxs-lookup"><span data-stu-id="fbf72-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="fbf72-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fbf72-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf72-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbf72-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="fbf72-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fbf72-112">Property value</span></span>

<span data-ttu-id="fbf72-113">Nombre de la canalización con nombre de la conexión RDP utilizada para el vídeo y la entrada.</span><span class="sxs-lookup"><span data-stu-id="fbf72-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbf72-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fbf72-114">Error codes</span></span>

<span data-ttu-id="fbf72-115">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fbf72-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbf72-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbf72-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="fbf72-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="fbf72-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="fbf72-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fbf72-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="fbf72-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fbf72-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fbf72-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fbf72-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="fbf72-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fbf72-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="fbf72-122">El parámetro RdpPipeName es **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf72-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="fbf72-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fbf72-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="fbf72-124">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="fbf72-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="fbf72-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fbf72-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fbf72-126">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="fbf72-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="fbf72-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf72-127">Requirements</span></span>



| <span data-ttu-id="fbf72-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf72-128">Requirement</span></span> | <span data-ttu-id="fbf72-129">Value</span><span class="sxs-lookup"><span data-stu-id="fbf72-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf72-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf72-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf72-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbf72-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbf72-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf72-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf72-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fbf72-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fbf72-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fbf72-134">End of client support</span></span><br/>    | <span data-ttu-id="fbf72-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbf72-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fbf72-136">Producto</span><span class="sxs-lookup"><span data-stu-id="fbf72-136">Product</span></span><br/>                  | <span data-ttu-id="fbf72-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fbf72-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fbf72-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbf72-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf72-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf72-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fbf72-140">IID</span><span class="sxs-lookup"><span data-stu-id="fbf72-140">IID</span></span><br/>                      | <span data-ttu-id="fbf72-141">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fbf72-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fbf72-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbf72-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf72-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fbf72-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

