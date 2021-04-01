---
title: Propiedad de recuento de IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera el número de puertos serie de esta colección.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMSerialPortCollection
- Interfaz IVMSerialPortCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905375"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="8a409-106">IVMSerialPortCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8a409-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="8a409-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8a409-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8a409-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8a409-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8a409-109">Recupera el número de puertos serie de esta colección.</span><span class="sxs-lookup"><span data-stu-id="8a409-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="8a409-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a409-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a409-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a409-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="8a409-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a409-112">Property value</span></span>

<span data-ttu-id="8a409-113">El número de puertos serie.</span><span class="sxs-lookup"><span data-stu-id="8a409-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a409-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8a409-114">Error codes</span></span>



| <span data-ttu-id="8a409-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="8a409-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="8a409-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8a409-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="8a409-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8a409-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="8a409-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a409-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="8a409-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8a409-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="8a409-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="8a409-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="8a409-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a409-121">Requirements</span></span>



| <span data-ttu-id="8a409-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a409-122">Requirement</span></span> | <span data-ttu-id="8a409-123">Value</span><span class="sxs-lookup"><span data-stu-id="8a409-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a409-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a409-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a409-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a409-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a409-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a409-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a409-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a409-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8a409-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8a409-128">End of client support</span></span><br/>    | <span data-ttu-id="8a409-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a409-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8a409-130">Producto</span><span class="sxs-lookup"><span data-stu-id="8a409-130">Product</span></span><br/>                  | <span data-ttu-id="8a409-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8a409-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8a409-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a409-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a409-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a409-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8a409-134">IID</span><span class="sxs-lookup"><span data-stu-id="8a409-134">IID</span></span><br/>                      | <span data-ttu-id="8a409-135">IID \_ IVMSerialPortCollection se define como dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="8a409-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="8a409-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a409-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a409-137">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="8a409-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

