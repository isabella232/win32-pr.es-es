---
title: Propiedad IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces. h)
description: Recupera un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Propiedad UndoHardDisk Virtual PC
- Propiedad UndoHardDisk Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, propiedad UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149863"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="4887f-106">IVMHardDiskConnection:: UndoHardDisk (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4887f-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="4887f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4887f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4887f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4887f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4887f-109">Recupera un objeto de disco duro correspondiente a la imagen de disco para deshacer de esta conexión.</span><span class="sxs-lookup"><span data-stu-id="4887f-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="4887f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4887f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4887f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4887f-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="4887f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4887f-112">Property value</span></span>

<span data-ttu-id="4887f-113">Un objeto [**IVMHardDisk**](ivmharddisk.md) que describe el disco duro para deshacer asociado a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="4887f-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4887f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4887f-114">Error codes</span></span>



| <span data-ttu-id="4887f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="4887f-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="4887f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4887f-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4887f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4887f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="4887f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4887f-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="4887f-119"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4887f-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="4887f-120">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="4887f-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="4887f-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4887f-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="4887f-122">El parámetro es **null** o no es válido.</span><span class="sxs-lookup"><span data-stu-id="4887f-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4887f-123"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="4887f-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="4887f-124">No se encontró el disco para deshacer para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="4887f-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4887f-125"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4887f-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="4887f-126">La configuración de máquina virtual actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="4887f-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="4887f-127"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4887f-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="4887f-128">La ubicación del bus para esta conexión no se ha inicializado correctamente o el dispositivo en esta ubicación no es un disco duro válido.</span><span class="sxs-lookup"><span data-stu-id="4887f-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4887f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4887f-129">Requirements</span></span>



| <span data-ttu-id="4887f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4887f-130">Requirement</span></span> | <span data-ttu-id="4887f-131">Value</span><span class="sxs-lookup"><span data-stu-id="4887f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4887f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4887f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4887f-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4887f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4887f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4887f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4887f-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4887f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4887f-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4887f-136">End of client support</span></span><br/>    | <span data-ttu-id="4887f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4887f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4887f-138">Producto</span><span class="sxs-lookup"><span data-stu-id="4887f-138">Product</span></span><br/>                  | <span data-ttu-id="4887f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4887f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4887f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4887f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4887f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4887f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4887f-142">IID</span><span class="sxs-lookup"><span data-stu-id="4887f-142">IID</span></span><br/>                      | <span data-ttu-id="4887f-143">IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="4887f-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="4887f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4887f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4887f-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="4887f-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

