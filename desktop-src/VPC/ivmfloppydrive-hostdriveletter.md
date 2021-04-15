---
title: Propiedad IVMFloppyDrive HostDriveLetter (VPCCOMInterfaces. h)
description: La letra de la unidad host a la que está conectada la unidad de disquete.
ms.assetid: 16d11e06-e3bc-4a4a-850d-f7b4122e6af9
keywords:
- Propiedad HostDriveLetter Virtual PC
- Propiedad HostDriveLetter Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, propiedad HostDriveLetter
topic_type:
- apiref
api_name:
- IVMFloppyDrive.HostDriveLetter
- IVMFloppyDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4896699dd3547eb3488e2fc085b5b2c54de827b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534288"
---
# <a name="ivmfloppydrivehostdriveletter-property"></a><span data-ttu-id="11491-106">IVMFloppyDrive:: HostDriveLetter (propiedad)</span><span class="sxs-lookup"><span data-stu-id="11491-106">IVMFloppyDrive::HostDriveLetter property</span></span>

<span data-ttu-id="11491-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="11491-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="11491-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="11491-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="11491-109">Recupera la letra de la unidad host a la que está conectada la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="11491-109">Retrieves the letter of the host drive to which the floppy drive is attached.</span></span>

<span data-ttu-id="11491-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11491-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11491-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11491-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="11491-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="11491-112">Property value</span></span>

<span data-ttu-id="11491-113">Letra de la unidad de disquete física.</span><span class="sxs-lookup"><span data-stu-id="11491-113">The letter of the physical floppy drive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11491-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="11491-114">Error codes</span></span>



| <span data-ttu-id="11491-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="11491-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="11491-116">Significado</span><span class="sxs-lookup"><span data-stu-id="11491-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11491-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11491-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="11491-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="11491-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="11491-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="11491-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="11491-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="11491-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="11491-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="11491-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="11491-122">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="11491-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="11491-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="11491-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="11491-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="11491-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="11491-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11491-125">Requirements</span></span>



| <span data-ttu-id="11491-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="11491-126">Requirement</span></span> | <span data-ttu-id="11491-127">Value</span><span class="sxs-lookup"><span data-stu-id="11491-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="11491-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11491-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11491-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="11491-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11491-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11491-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11491-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="11491-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="11491-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="11491-132">End of client support</span></span><br/>    | <span data-ttu-id="11491-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="11491-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="11491-134">Producto</span><span class="sxs-lookup"><span data-stu-id="11491-134">Product</span></span><br/>                  | <span data-ttu-id="11491-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="11491-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="11491-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11491-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="11491-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="11491-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="11491-138">IID</span><span class="sxs-lookup"><span data-stu-id="11491-138">IID</span></span><br/>                      | <span data-ttu-id="11491-139">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="11491-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="11491-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="11491-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11491-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="11491-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

