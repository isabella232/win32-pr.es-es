---
title: Propiedad IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces. h)
description: Acción que se realizará en esta máquina virtual si se ejecuta cuando se cierra Windows Virtual PC.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Propiedad ShutdownActionOnQuit Virtual PC
- Propiedad ShutdownActionOnQuit Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492221"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="0b57e-106">IVMVirtualMachine:: ShutdownActionOnQuit (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0b57e-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="0b57e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b57e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b57e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b57e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b57e-109">Recupera y establece la acción que se realizará en esta máquina virtual (VM) si se ejecuta cuando se cierra Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0b57e-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="0b57e-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0b57e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b57e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b57e-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="0b57e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b57e-112">Property value</span></span>

<span data-ttu-id="0b57e-113">Especifica cómo apagar la máquina virtual si se ejecuta cuando se cierra Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0b57e-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="0b57e-114">Para obtener una lista de valores, vea [**VMShutdownAction**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="0b57e-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b57e-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0b57e-115">Error codes</span></span>



| <span data-ttu-id="0b57e-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="0b57e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0b57e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0b57e-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b57e-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0b57e-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b57e-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="0b57e-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0b57e-121">El parámetro es **null** o no es un valor válido.</span><span class="sxs-lookup"><span data-stu-id="0b57e-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="0b57e-122"><dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="0b57e-123">El usuario actual no tiene acceso suficiente al archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="0b57e-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="0b57e-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0b57e-125">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="0b57e-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="0b57e-126"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0b57e-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b57e-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="0b57e-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b57e-128">Remarks</span></span>

<span data-ttu-id="0b57e-129">De forma predeterminada, las máquinas virtuales en ejecución se guardan cuando se sale de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0b57e-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="0b57e-130">La acción de apagado **vmShutdownAction \_ Save** (0) guardará el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b57e-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="0b57e-131">La acción de desactivación de **vmShutdownAction \_** (1) desconectará la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b57e-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="0b57e-132">La acción de **\_ cierre de vmShutdownAction** (2) apagará el sistema operativo invitado si los componentes de integración están disponibles y guardará la máquina virtual en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0b57e-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b57e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b57e-133">Requirements</span></span>



| <span data-ttu-id="0b57e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b57e-134">Requirement</span></span> | <span data-ttu-id="0b57e-135">Value</span><span class="sxs-lookup"><span data-stu-id="0b57e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b57e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b57e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b57e-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b57e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b57e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b57e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b57e-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b57e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b57e-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0b57e-140">End of client support</span></span><br/>    | <span data-ttu-id="0b57e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b57e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b57e-142">Producto</span><span class="sxs-lookup"><span data-stu-id="0b57e-142">Product</span></span><br/>                  | <span data-ttu-id="0b57e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b57e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b57e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b57e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b57e-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b57e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b57e-146">IID</span><span class="sxs-lookup"><span data-stu-id="0b57e-146">IID</span></span><br/>                      | <span data-ttu-id="0b57e-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0b57e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0b57e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b57e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b57e-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0b57e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="0b57e-150">**VMShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="0b57e-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

