---
title: Propiedad IVMSerialPort ConnectImmediately (VPCCOMInterfaces. h)
description: Determina si el puerto serie debe abrirse sin esperar a que se reciba un comando de módem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Propiedad ConnectImmediately Virtual PC
- Propiedad ConnectImmediately Virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, propiedad ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802456"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="fe8c3-106">IVMSerialPort:: ConnectImmediately (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fe8c3-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="fe8c3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fe8c3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fe8c3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fe8c3-109">Determina si el puerto serie debe abrirse sin esperar a que se reciba un comando de módem.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="fe8c3-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8c3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe8c3-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="fe8c3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fe8c3-112">Property value</span></span>

<span data-ttu-id="fe8c3-113">**Variante \_ TRUE** si se debe abrir el puerto serie sin esperar a que se reciba un comando de módem; **Variante \_** De lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe8c3-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fe8c3-114">Error codes</span></span>



| <span data-ttu-id="fe8c3-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="fe8c3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fe8c3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fe8c3-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe8c3-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fe8c3-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="fe8c3-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fe8c3-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="fe8c3-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fe8c3-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="fe8c3-122">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="fe8c3-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c3-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fe8c3-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="fe8c3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe8c3-125">Remarks</span></span>

<span data-ttu-id="fe8c3-126">Esta propiedad solo es válida si la propiedad de [**tipo**](ivmserialport-type.md) de puerto es **vmSerialPort \_ denominaba hostport**.</span><span class="sxs-lookup"><span data-stu-id="fe8c3-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8c3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe8c3-127">Requirements</span></span>



| <span data-ttu-id="fe8c3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8c3-128">Requirement</span></span> | <span data-ttu-id="fe8c3-129">Value</span><span class="sxs-lookup"><span data-stu-id="fe8c3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8c3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe8c3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8c3-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe8c3-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe8c3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe8c3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8c3-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe8c3-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fe8c3-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fe8c3-134">End of client support</span></span><br/>    | <span data-ttu-id="fe8c3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe8c3-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fe8c3-136">Producto</span><span class="sxs-lookup"><span data-stu-id="fe8c3-136">Product</span></span><br/>                  | <span data-ttu-id="fe8c3-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fe8c3-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fe8c3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe8c3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8c3-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8c3-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fe8c3-140">IID</span><span class="sxs-lookup"><span data-stu-id="fe8c3-140">IID</span></span><br/>                      | <span data-ttu-id="fe8c3-141">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="fe8c3-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="fe8c3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe8c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8c3-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="fe8c3-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

