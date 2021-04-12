---
title: Interfaz IVMSerialPort (VPCCOMInterfaces. h)
description: Define un puerto serie dentro de una máquina virtual.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Interfaz IVMSerialPort Virtual PC
- Interfaz IVMSerialPort Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534780"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="69c2c-105">Interfaz IVMSerialPort</span><span class="sxs-lookup"><span data-stu-id="69c2c-105">IVMSerialPort interface</span></span>

<span data-ttu-id="69c2c-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="69c2c-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69c2c-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69c2c-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69c2c-108">Define un puerto serie dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69c2c-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="69c2c-109">Esta interfaz permite configurar puertos serie dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69c2c-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="69c2c-110">Puede recuperar un objeto **IVMSerialPort** del objeto [**IVMSerialPortCollection**](ivmserialportcollection.md) devuelto desde la propiedad [**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="69c2c-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="69c2c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="69c2c-111">Members</span></span>

<span data-ttu-id="69c2c-112">La interfaz **IVMSerialPort** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="69c2c-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="69c2c-113">**IVMSerialPort** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="69c2c-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="69c2c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="69c2c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="69c2c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69c2c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="69c2c-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="69c2c-116">Methods</span></span>

<span data-ttu-id="69c2c-117">La interfaz **IVMSerialPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="69c2c-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="69c2c-118">Método</span><span class="sxs-lookup"><span data-stu-id="69c2c-118">Method</span></span>                                       | <span data-ttu-id="69c2c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="69c2c-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="69c2c-120">**\_id**</span><span class="sxs-lookup"><span data-stu-id="69c2c-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="69c2c-121">Recupera el identificador interno del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="69c2c-122">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="69c2c-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="69c2c-123">Configura el puerto serie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="69c2c-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69c2c-124">Properties</span></span>

<span data-ttu-id="69c2c-125">La interfaz **IVMSerialPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="69c2c-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="69c2c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69c2c-126">Property</span></span>                                                                  | <span data-ttu-id="69c2c-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="69c2c-127">Access type</span></span>          | <span data-ttu-id="69c2c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="69c2c-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69c2c-129">**ConnectImmediately**</span><span class="sxs-lookup"><span data-stu-id="69c2c-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="69c2c-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="69c2c-130">Read-only</span></span><br/> | <span data-ttu-id="69c2c-131">Indica si se debe abrir el puerto serie sin esperar a que se reciba un comando de módem.</span><span class="sxs-lookup"><span data-stu-id="69c2c-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="69c2c-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="69c2c-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="69c2c-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="69c2c-133">Read-only</span></span><br/> | <span data-ttu-id="69c2c-134">Nombre del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="69c2c-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="69c2c-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="69c2c-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="69c2c-136">Read-only</span></span><br/> | <span data-ttu-id="69c2c-137">Tipo del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="69c2c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c2c-138">Requirements</span></span>



| <span data-ttu-id="69c2c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c2c-139">Requirement</span></span> | <span data-ttu-id="69c2c-140">Value</span><span class="sxs-lookup"><span data-stu-id="69c2c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c2c-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69c2c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="69c2c-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="69c2c-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69c2c-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69c2c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="69c2c-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="69c2c-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69c2c-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="69c2c-145">End of client support</span></span><br/>    | <span data-ttu-id="69c2c-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69c2c-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69c2c-147">Producto</span><span class="sxs-lookup"><span data-stu-id="69c2c-147">Product</span></span><br/>                  | <span data-ttu-id="69c2c-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69c2c-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69c2c-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69c2c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c2c-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c2c-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69c2c-151">IID</span><span class="sxs-lookup"><span data-stu-id="69c2c-151">IID</span></span><br/>                      | <span data-ttu-id="69c2c-152">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="69c2c-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

