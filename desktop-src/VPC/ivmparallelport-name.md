---
title: Propiedad nombre de IVMParallelPort (VPCCOMInterfaces. h)
description: Nombre del puerto paralelo.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMParallelPort
- Interfaz IVMParallelPort Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149855"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="dd3bf-106">IVMParallelPort:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dd3bf-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="dd3bf-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd3bf-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd3bf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd3bf-109">Recupera y establece el nombre del puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="dd3bf-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3bf-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd3bf-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="dd3bf-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dd3bf-112">Property value</span></span>

<span data-ttu-id="dd3bf-113">Establece el nombre del puerto paralelo (por ejemplo, "LPT1").</span><span class="sxs-lookup"><span data-stu-id="dd3bf-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd3bf-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="dd3bf-114">Error codes</span></span>



| <span data-ttu-id="dd3bf-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="dd3bf-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dd3bf-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dd3bf-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd3bf-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dd3bf-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="dd3bf-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dd3bf-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dd3bf-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="dd3bf-122">El parámetro hace referencia a un puerto paralelo que no es válido.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="dd3bf-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="dd3bf-124">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="dd3bf-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dd3bf-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="dd3bf-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="dd3bf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd3bf-127">Requirements</span></span>



| <span data-ttu-id="dd3bf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd3bf-128">Requirement</span></span> | <span data-ttu-id="dd3bf-129">Value</span><span class="sxs-lookup"><span data-stu-id="dd3bf-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3bf-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3bf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3bf-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3bf-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd3bf-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3bf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3bf-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dd3bf-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd3bf-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dd3bf-134">End of client support</span></span><br/>    | <span data-ttu-id="dd3bf-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd3bf-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd3bf-136">Producto</span><span class="sxs-lookup"><span data-stu-id="dd3bf-136">Product</span></span><br/>                  | <span data-ttu-id="dd3bf-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd3bf-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd3bf-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd3bf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3bf-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3bf-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dd3bf-140">IID</span><span class="sxs-lookup"><span data-stu-id="dd3bf-140">IID</span></span><br/>                      | <span data-ttu-id="dd3bf-141">IID \_ IVMParallelPort se define como 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="dd3bf-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="dd3bf-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd3bf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3bf-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="dd3bf-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

