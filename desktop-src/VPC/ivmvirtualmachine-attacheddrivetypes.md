---
title: Propiedad IVMVirtualMachine AttachedDriveTypes (VPCCOMInterfaces. h)
description: Una matriz que indica el tipo de unidad conectada a cada ubicación de la máquina virtual.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Propiedad AttachedDriveTypes Virtual PC
- Propiedad AttachedDriveTypes Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad AttachedDriveTypes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150944"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="671df-106">IVMVirtualMachine:: AttachedDriveTypes (propiedad)</span><span class="sxs-lookup"><span data-stu-id="671df-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="671df-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="671df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="671df-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="671df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="671df-109">Recupera una matriz que indica el tipo de unidad conectada a cada ubicación de la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="671df-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="671df-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="671df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="671df-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="671df-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="671df-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="671df-112">Property value</span></span>

<span data-ttu-id="671df-113">Una variante de tipo VT de **\_ matriz** VT \| **\_** que contiene entradas de tipo **VT \_ UI1**.</span><span class="sxs-lookup"><span data-stu-id="671df-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="671df-114">La matriz contiene el valor [**VMDriveType**](vmdrivetype.md) de cada dispositivo conectado a cada ubicación de bus.</span><span class="sxs-lookup"><span data-stu-id="671df-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="671df-115">La matriz está ordenada por \[  \] \[ *deviceID* busNumber \] .</span><span class="sxs-lookup"><span data-stu-id="671df-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="671df-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="671df-116">Error codes</span></span>



| <span data-ttu-id="671df-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="671df-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="671df-118">Significado</span><span class="sxs-lookup"><span data-stu-id="671df-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="671df-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="671df-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="671df-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="671df-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="671df-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="671df-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="671df-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="671df-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="671df-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="671df-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="671df-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="671df-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="671df-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="671df-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="671df-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="671df-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="671df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671df-127">Requirements</span></span>



| <span data-ttu-id="671df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="671df-128">Requirement</span></span> | <span data-ttu-id="671df-129">Value</span><span class="sxs-lookup"><span data-stu-id="671df-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="671df-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="671df-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="671df-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="671df-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="671df-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="671df-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="671df-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="671df-134">End of client support</span></span><br/>    | <span data-ttu-id="671df-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="671df-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="671df-136">Producto</span><span class="sxs-lookup"><span data-stu-id="671df-136">Product</span></span><br/>                  | <span data-ttu-id="671df-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="671df-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="671df-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="671df-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="671df-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="671df-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="671df-140">IID</span><span class="sxs-lookup"><span data-stu-id="671df-140">IID</span></span><br/>                      | <span data-ttu-id="671df-141">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="671df-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="671df-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="671df-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671df-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="671df-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

