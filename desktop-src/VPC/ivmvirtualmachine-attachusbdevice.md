---
title: Método IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Conecta un dispositivo USB a una máquina virtual.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Método AttachUSBDevice Virtual PC
- Método AttachUSBDevice Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079502"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="81ba2-106">IVMVirtualMachine:: AttachUSBDevice (método)</span><span class="sxs-lookup"><span data-stu-id="81ba2-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="81ba2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="81ba2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="81ba2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="81ba2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="81ba2-109">Conecta un dispositivo USB a una máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="81ba2-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="81ba2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81ba2-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="81ba2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81ba2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ba2-112">*inUSBDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81ba2-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ba2-113">Un puntero [**IVMUSBDevice**](ivmusbdevice.md) que representa el dispositivo USB conectado al host.</span><span class="sxs-lookup"><span data-stu-id="81ba2-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ba2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81ba2-114">Return value</span></span>

<span data-ttu-id="81ba2-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="81ba2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="81ba2-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81ba2-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="81ba2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="81ba2-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81ba2-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="81ba2-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="81ba2-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="81ba2-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="81ba2-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="81ba2-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="81ba2-122"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="81ba2-123">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="81ba2-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="81ba2-124"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="81ba2-125">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="81ba2-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="81ba2-126"><dt>**Máquina virtual \_ E/s \_ \_ no \_ DISP**</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="81ba2-127">Los componentes de integración no están disponibles en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="81ba2-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="81ba2-128"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="81ba2-129">La característica USB no está disponible.</span><span class="sxs-lookup"><span data-stu-id="81ba2-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="81ba2-130"><dt>**Máquina virtual \_ \_Error del \_ \_ controlador \_ del conector de E USB**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="81ba2-131">Error en el controlador del conector USB.</span><span class="sxs-lookup"><span data-stu-id="81ba2-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="81ba2-132"><dt>**Máquina virtual \_ E \_ conexión USB con \_ \_ errores \_ más \_ dispositivos**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="81ba2-133">No se pueden conectar más dispositivos a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="81ba2-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="81ba2-134"><dt>**Máquina virtual \_ E \_ \_ \_ \_ \_ error de directiva**</dt> de <dt>0xA00400932</dt> de conexión USB</span><span class="sxs-lookup"><span data-stu-id="81ba2-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="81ba2-135">Una configuración de directiva de grupo impide el redireccionamiento USB.</span><span class="sxs-lookup"><span data-stu-id="81ba2-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="81ba2-136"><dt>**Máquina virtual \_ \_ \_ \_ \_ \_ Error al adjuntar USB**</dt> <dt>0xA00400933</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="81ba2-137">Otro cliente ya ha conectado un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="81ba2-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="81ba2-138"><dt>**Máquina virtual \_ E \_ \_ \_ no se pudo adjuntar USB**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="81ba2-139">Error en la operación de adjuntar.</span><span class="sxs-lookup"><span data-stu-id="81ba2-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="81ba2-140"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="81ba2-141">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="81ba2-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="81ba2-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ba2-142">Requirements</span></span>



| <span data-ttu-id="81ba2-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ba2-143">Requirement</span></span> | <span data-ttu-id="81ba2-144">Value</span><span class="sxs-lookup"><span data-stu-id="81ba2-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ba2-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ba2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="81ba2-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="81ba2-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81ba2-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ba2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="81ba2-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81ba2-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="81ba2-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="81ba2-149">End of client support</span></span><br/>    | <span data-ttu-id="81ba2-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81ba2-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="81ba2-151">Producto</span><span class="sxs-lookup"><span data-stu-id="81ba2-151">Product</span></span><br/>                  | <span data-ttu-id="81ba2-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="81ba2-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="81ba2-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81ba2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ba2-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ba2-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="81ba2-155">IID</span><span class="sxs-lookup"><span data-stu-id="81ba2-155">IID</span></span><br/>                      | <span data-ttu-id="81ba2-156">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="81ba2-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="81ba2-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="81ba2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ba2-158">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="81ba2-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

