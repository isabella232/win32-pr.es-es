---
title: Propiedad IVMHostInfo UTCTime (VPCCOMInterfaces. h)
description: Recupera la hora UTC en el equipo host.
ms.assetid: 07f9b042-0eb6-4cb5-b70b-6fcd3456d46b
keywords:
- Propiedad UTCTime Virtual PC
- Propiedad UTCTime Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad UTCTime
topic_type:
- apiref
api_name:
- IVMHostInfo.UTCTime
- IVMHostInfo.get_UTCTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd913db320f24446de6b72dd220f2c67713a16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534246"
---
# <a name="ivmhostinfoutctime-property"></a><span data-ttu-id="79605-106">IVMHostInfo:: UTCTime (propiedad)</span><span class="sxs-lookup"><span data-stu-id="79605-106">IVMHostInfo::UTCTime property</span></span>

<span data-ttu-id="79605-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79605-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79605-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79605-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79605-109">Recupera la hora UTC en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="79605-109">Retrieves the UTC time on the host machine.</span></span>

<span data-ttu-id="79605-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="79605-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79605-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79605-111">Syntax</span></span>


```C++
HRESULT get_UTCTime(
  [out, retval] DATE *UTCTime
);
```



## <a name="property-value"></a><span data-ttu-id="79605-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="79605-112">Property value</span></span>

<span data-ttu-id="79605-113">Hora UTC actual.</span><span class="sxs-lookup"><span data-stu-id="79605-113">The current UTC time.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79605-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="79605-114">Error codes</span></span>



| <span data-ttu-id="79605-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="79605-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="79605-116">Significado</span><span class="sxs-lookup"><span data-stu-id="79605-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="79605-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79605-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="79605-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79605-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="79605-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="79605-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="79605-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="79605-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="79605-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="79605-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="79605-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="79605-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="79605-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79605-123">Requirements</span></span>



| <span data-ttu-id="79605-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79605-124">Requirement</span></span> | <span data-ttu-id="79605-125">Value</span><span class="sxs-lookup"><span data-stu-id="79605-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79605-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79605-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79605-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="79605-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79605-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79605-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79605-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79605-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79605-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="79605-130">End of client support</span></span><br/>    | <span data-ttu-id="79605-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79605-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79605-132">Producto</span><span class="sxs-lookup"><span data-stu-id="79605-132">Product</span></span><br/>                  | <span data-ttu-id="79605-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79605-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79605-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79605-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="79605-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79605-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79605-136">IID</span><span class="sxs-lookup"><span data-stu-id="79605-136">IID</span></span><br/>                      | <span data-ttu-id="79605-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="79605-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="79605-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="79605-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79605-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="79605-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

