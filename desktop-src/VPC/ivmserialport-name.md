---
title: Propiedad nombre de IVMSerialPort (VPCCOMInterfaces. h)
description: Nombre del puerto serie.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905531"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="55472-106">IVMSerialPort:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="55472-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="55472-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55472-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="55472-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="55472-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="55472-109">Recupera el nombre del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="55472-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="55472-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="55472-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55472-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55472-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="55472-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="55472-112">Property value</span></span>

<span data-ttu-id="55472-113">Nombre del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="55472-113">The name of the serial port.</span></span> <span data-ttu-id="55472-114">Por ejemplo, "COM1" para **vmSerialPort \_ denominaba hostport**, "C: \\SerialPort.txt" para **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ Pipe \\ *pipename*" para **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="55472-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55472-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="55472-115">Error codes</span></span>



| <span data-ttu-id="55472-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="55472-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="55472-117">Significado</span><span class="sxs-lookup"><span data-stu-id="55472-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="55472-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="55472-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="55472-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="55472-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="55472-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="55472-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="55472-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="55472-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="55472-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="55472-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="55472-123">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="55472-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="55472-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="55472-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="55472-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="55472-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="55472-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55472-126">Requirements</span></span>



| <span data-ttu-id="55472-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="55472-127">Requirement</span></span> | <span data-ttu-id="55472-128">Value</span><span class="sxs-lookup"><span data-stu-id="55472-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55472-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55472-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55472-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="55472-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55472-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55472-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55472-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55472-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="55472-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="55472-133">End of client support</span></span><br/>    | <span data-ttu-id="55472-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55472-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="55472-135">Producto</span><span class="sxs-lookup"><span data-stu-id="55472-135">Product</span></span><br/>                  | <span data-ttu-id="55472-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55472-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="55472-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55472-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="55472-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="55472-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="55472-139">IID</span><span class="sxs-lookup"><span data-stu-id="55472-139">IID</span></span><br/>                      | <span data-ttu-id="55472-140">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="55472-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="55472-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="55472-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55472-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="55472-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

