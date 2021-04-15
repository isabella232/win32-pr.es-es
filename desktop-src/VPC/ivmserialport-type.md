---
title: Propiedad de tipo IVMSerialPort (VPCCOMInterfaces. h)
description: Recupera el tipo del puerto serie.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Propiedad de tipo Virtual PC
- Propiedad Type Virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, propiedad de tipo
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490954"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="bb06a-106">IVMSerialPort:: Type (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bb06a-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="bb06a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb06a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb06a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb06a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb06a-109">Recupera el tipo del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="bb06a-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="bb06a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb06a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb06a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb06a-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="bb06a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bb06a-112">Property value</span></span>

<span data-ttu-id="bb06a-113">El tipo de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="bb06a-113">The type of serial port.</span></span> <span data-ttu-id="bb06a-114">Para obtener una lista de valores, vea [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="bb06a-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb06a-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bb06a-115">Error codes</span></span>



| <span data-ttu-id="bb06a-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="bb06a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bb06a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="bb06a-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb06a-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb06a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bb06a-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb06a-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="bb06a-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bb06a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bb06a-121">El parámetro es NULL.</span><span class="sxs-lookup"><span data-stu-id="bb06a-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bb06a-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bb06a-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="bb06a-123">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="bb06a-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="bb06a-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bb06a-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bb06a-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="bb06a-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="bb06a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb06a-126">Requirements</span></span>



| <span data-ttu-id="bb06a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb06a-127">Requirement</span></span> | <span data-ttu-id="bb06a-128">Value</span><span class="sxs-lookup"><span data-stu-id="bb06a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb06a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb06a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bb06a-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb06a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb06a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb06a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bb06a-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bb06a-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb06a-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bb06a-133">End of client support</span></span><br/>    | <span data-ttu-id="bb06a-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb06a-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb06a-135">Producto</span><span class="sxs-lookup"><span data-stu-id="bb06a-135">Product</span></span><br/>                  | <span data-ttu-id="bb06a-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb06a-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb06a-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb06a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb06a-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb06a-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb06a-139">IID</span><span class="sxs-lookup"><span data-stu-id="bb06a-139">IID</span></span><br/>                      | <span data-ttu-id="bb06a-140">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="bb06a-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="bb06a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb06a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb06a-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="bb06a-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

