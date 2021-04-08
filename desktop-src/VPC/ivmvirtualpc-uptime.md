---
title: Propiedad de tiempo de actividad de IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera el número de segundos que se ha estado ejecutando la aplicación Windows Virtual PC.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- Propiedad de tiempo de actividad Virtual PC
- Propiedad de tiempo de actividad Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad de tiempo de actividad
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803728"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="7477a-106">IVMVirtualPC:: tiempo de actividad (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7477a-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="7477a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7477a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7477a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7477a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7477a-109">Recupera el número de segundos que se ha estado ejecutando la aplicación Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7477a-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="7477a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7477a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7477a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7477a-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="7477a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7477a-112">Property value</span></span>

<span data-ttu-id="7477a-113">El número de segundos que se ha estado ejecutando la aplicación Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7477a-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7477a-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7477a-114">Error codes</span></span>



| <span data-ttu-id="7477a-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="7477a-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="7477a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7477a-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7477a-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7477a-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7477a-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7477a-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="7477a-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="7477a-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7477a-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="7477a-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="7477a-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="7477a-123"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="7477a-124">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="7477a-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7477a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7477a-125">Requirements</span></span>



| <span data-ttu-id="7477a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7477a-126">Requirement</span></span> | <span data-ttu-id="7477a-127">Value</span><span class="sxs-lookup"><span data-stu-id="7477a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7477a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7477a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7477a-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7477a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7477a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7477a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7477a-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7477a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7477a-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7477a-132">End of client support</span></span><br/>    | <span data-ttu-id="7477a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7477a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7477a-134">Producto</span><span class="sxs-lookup"><span data-stu-id="7477a-134">Product</span></span><br/>                  | <span data-ttu-id="7477a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7477a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7477a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7477a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7477a-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7477a-138">IID</span><span class="sxs-lookup"><span data-stu-id="7477a-138">IID</span></span><br/>                      | <span data-ttu-id="7477a-139">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7477a-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7477a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7477a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7477a-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="7477a-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

