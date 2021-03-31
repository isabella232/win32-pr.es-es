---
title: Método IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces. h)
description: Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Método OnConfigurationChanged Virtual PC
- Método OnConfigurationChanged Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnConfigurationChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995893"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="6057d-106">IVMVirtualMachineEvents:: OnConfigurationChanged (método)</span><span class="sxs-lookup"><span data-stu-id="6057d-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="6057d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6057d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6057d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6057d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6057d-109">Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6057d-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6057d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6057d-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="6057d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6057d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6057d-112">*configKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6057d-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6057d-113">Valor dentro de la configuración que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6057d-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="6057d-114">*configData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6057d-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6057d-115">Nuevo valor de la configuración.</span><span class="sxs-lookup"><span data-stu-id="6057d-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6057d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6057d-116">Return value</span></span>

<span data-ttu-id="6057d-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6057d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6057d-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6057d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6057d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6057d-119">Remarks</span></span>

<span data-ttu-id="6057d-120">Se llama a este método cuando cambia la configuración de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6057d-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="6057d-121">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmVirtualMachineEvent ConfigurationChanged que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="6057d-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6057d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6057d-122">Requirements</span></span>



| <span data-ttu-id="6057d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6057d-123">Requirement</span></span> | <span data-ttu-id="6057d-124">Value</span><span class="sxs-lookup"><span data-stu-id="6057d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6057d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6057d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6057d-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6057d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6057d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6057d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6057d-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6057d-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6057d-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6057d-129">End of client support</span></span><br/>    | <span data-ttu-id="6057d-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6057d-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6057d-131">Producto</span><span class="sxs-lookup"><span data-stu-id="6057d-131">Product</span></span><br/>                  | <span data-ttu-id="6057d-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6057d-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6057d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6057d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6057d-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6057d-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6057d-135">IID</span><span class="sxs-lookup"><span data-stu-id="6057d-135">IID</span></span><br/>                      | <span data-ttu-id="6057d-136">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="6057d-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="6057d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6057d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6057d-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="6057d-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

