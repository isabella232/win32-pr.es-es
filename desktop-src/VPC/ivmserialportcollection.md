---
title: Interfaz IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Define la colección de puertos serie dentro de la máquina virtual. Para obtener un objeto IVMSerialPortCollection, use la propiedad SerialPorts de IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Interfaz IVMSerialPortCollection Virtual PC
- Interfaz IVMSerialPortCollection Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802455"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="821b2-106">Interfaz IVMSerialPortCollection</span><span class="sxs-lookup"><span data-stu-id="821b2-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="821b2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="821b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="821b2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="821b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="821b2-109">Define la colección de puertos serie dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="821b2-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="821b2-110">Para obtener un objeto **IVMSerialPortCollection** , use la propiedad [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="821b2-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="821b2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="821b2-111">Members</span></span>

<span data-ttu-id="821b2-112">La interfaz **IVMSerialPortCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="821b2-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="821b2-113">**IVMSerialPortCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="821b2-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="821b2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="821b2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="821b2-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="821b2-115">Properties</span></span>

<span data-ttu-id="821b2-116">La interfaz **IVMSerialPortCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="821b2-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="821b2-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="821b2-117">Property</span></span>                                                         | <span data-ttu-id="821b2-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="821b2-118">Access type</span></span>          | <span data-ttu-id="821b2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="821b2-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="821b2-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="821b2-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="821b2-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="821b2-121">Read-only</span></span><br/> | <span data-ttu-id="821b2-122">Un enumerador de la colección.</span><span class="sxs-lookup"><span data-stu-id="821b2-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="821b2-123">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="821b2-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="821b2-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="821b2-124">Read-only</span></span><br/> | <span data-ttu-id="821b2-125">Número de puertos serie de esta colección.</span><span class="sxs-lookup"><span data-stu-id="821b2-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="821b2-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="821b2-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="821b2-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="821b2-127">Read-only</span></span><br/> | <span data-ttu-id="821b2-128">Objeto de puerto serie que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="821b2-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="821b2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="821b2-129">Requirements</span></span>



| <span data-ttu-id="821b2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="821b2-130">Requirement</span></span> | <span data-ttu-id="821b2-131">Value</span><span class="sxs-lookup"><span data-stu-id="821b2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="821b2-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="821b2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="821b2-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="821b2-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="821b2-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="821b2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="821b2-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="821b2-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="821b2-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="821b2-136">End of client support</span></span><br/>    | <span data-ttu-id="821b2-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="821b2-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="821b2-138">Producto</span><span class="sxs-lookup"><span data-stu-id="821b2-138">Product</span></span><br/>                  | <span data-ttu-id="821b2-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="821b2-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="821b2-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="821b2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="821b2-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="821b2-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="821b2-142">IID</span><span class="sxs-lookup"><span data-stu-id="821b2-142">IID</span></span><br/>                      | <span data-ttu-id="821b2-143">IID \_ IVMSerialPortCollection se define como dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="821b2-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="821b2-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="821b2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821b2-145">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="821b2-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="821b2-146">**IVMVirtualMachine::SerialPorts**</span><span class="sxs-lookup"><span data-stu-id="821b2-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

