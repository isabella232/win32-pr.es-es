---
title: Propiedad IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
description: La letra de la unidad de host establecida para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Propiedad HostDriveLetter Virtual PC
- Propiedad HostDriveLetter Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801970"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="0b5c7-106">IVMDVDDrive:: HostDriveLetter (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0b5c7-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="0b5c7-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b5c7-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b5c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b5c7-109">Recupera la letra de la unidad de host establecida para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="0b5c7-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b5c7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b5c7-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="0b5c7-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b5c7-112">Property value</span></span>

<span data-ttu-id="0b5c7-113">Letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b5c7-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0b5c7-114">Error codes</span></span>



| <span data-ttu-id="0b5c7-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="0b5c7-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="0b5c7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0b5c7-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b5c7-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="0b5c7-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="0b5c7-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="0b5c7-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="0b5c7-121"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="0b5c7-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="0b5c7-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="0b5c7-124">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="0b5c7-125"><dt>Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="0b5c7-126">El medio capturado por esta unidad de DVD no es una unidad de host.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="0b5c7-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="0b5c7-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0b5c7-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="0b5c7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b5c7-129">Requirements</span></span>



| <span data-ttu-id="0b5c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b5c7-130">Requirement</span></span> | <span data-ttu-id="0b5c7-131">Value</span><span class="sxs-lookup"><span data-stu-id="0b5c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5c7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b5c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5c7-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b5c7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b5c7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b5c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5c7-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b5c7-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b5c7-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0b5c7-136">End of client support</span></span><br/>    | <span data-ttu-id="0b5c7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b5c7-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b5c7-138">Producto</span><span class="sxs-lookup"><span data-stu-id="0b5c7-138">Product</span></span><br/>                  | <span data-ttu-id="0b5c7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b5c7-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b5c7-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b5c7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b5c7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b5c7-142">IID</span><span class="sxs-lookup"><span data-stu-id="0b5c7-142">IID</span></span><br/>                      | <span data-ttu-id="0b5c7-143">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="0b5c7-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0b5c7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b5c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b5c7-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="0b5c7-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

