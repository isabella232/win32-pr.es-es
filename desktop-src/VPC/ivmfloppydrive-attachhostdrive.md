---
title: Método IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Conecta una unidad física del host a la unidad de disquete en la máquina virtual.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Método AttachHostDrive Virtual PC
- Método AttachHostDrive Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079507"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="df980-106">IVMFloppyDrive:: AttachHostDrive (método)</span><span class="sxs-lookup"><span data-stu-id="df980-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="df980-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="df980-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="df980-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="df980-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="df980-109">Conecta una unidad física del host a la unidad de disquete en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df980-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="df980-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df980-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="df980-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df980-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df980-112">*letraDeUnidad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df980-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df980-113">La letra de unidad de la unidad de disquete física en el equipo host que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="df980-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df980-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df980-114">Return value</span></span>

<span data-ttu-id="df980-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="df980-115">This method can return one of these values.</span></span>



| <span data-ttu-id="df980-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df980-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="df980-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="df980-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df980-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="df980-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="df980-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="df980-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="df980-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="df980-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="df980-121">El parámetro *letraDeUnidad* es **null**, no es una unidad de disquete válida o la ruta de acceso especificada está vacía.</span><span class="sxs-lookup"><span data-stu-id="df980-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="df980-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df980-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="df980-123">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="df980-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="df980-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="df980-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="df980-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="df980-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="df980-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df980-126">Requirements</span></span>



| <span data-ttu-id="df980-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df980-127">Requirement</span></span> | <span data-ttu-id="df980-128">Value</span><span class="sxs-lookup"><span data-stu-id="df980-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="df980-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df980-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df980-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="df980-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df980-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df980-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df980-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="df980-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="df980-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="df980-133">End of client support</span></span><br/>    | <span data-ttu-id="df980-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df980-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="df980-135">Producto</span><span class="sxs-lookup"><span data-stu-id="df980-135">Product</span></span><br/>                  | <span data-ttu-id="df980-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="df980-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="df980-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df980-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="df980-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="df980-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="df980-139">IID</span><span class="sxs-lookup"><span data-stu-id="df980-139">IID</span></span><br/>                      | <span data-ttu-id="df980-140">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="df980-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="df980-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="df980-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df980-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="df980-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

