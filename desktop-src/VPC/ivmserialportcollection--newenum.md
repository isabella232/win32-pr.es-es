---
title: Propiedad _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
ms.assetid: 4bf7bbde-d97f-424e-afa0-ff0e334740b5
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMSerialPortCollection
- Interfaz IVMSerialPortCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMSerialPortCollection._NewEnum
- IVMSerialPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fdfc2b300823c674cf5d4fd8e36dffeb58f8c1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547763"
---
# <a name="ivmserialportcollection_newenum-property"></a><span data-ttu-id="23cdf-107">IVMSerialPortCollection:: \_ NewEnum (propiedad)</span><span class="sxs-lookup"><span data-stu-id="23cdf-107">IVMSerialPortCollection::\_NewEnum property</span></span>

<span data-ttu-id="23cdf-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="23cdf-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="23cdf-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="23cdf-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="23cdf-110">Recupera un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="23cdf-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="23cdf-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="23cdf-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cdf-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23cdf-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="23cdf-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="23cdf-113">Property value</span></span>

<span data-ttu-id="23cdf-114">Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="23cdf-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23cdf-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="23cdf-115">Error codes</span></span>



| <span data-ttu-id="23cdf-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="23cdf-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="23cdf-117">Significado</span><span class="sxs-lookup"><span data-stu-id="23cdf-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="23cdf-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23cdf-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="23cdf-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="23cdf-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="23cdf-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="23cdf-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="23cdf-121">El parámetro es NULL.</span><span class="sxs-lookup"><span data-stu-id="23cdf-121">The parameter is NULL.</span></span><br/>        |
| <dl> <span data-ttu-id="23cdf-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="23cdf-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="23cdf-123">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="23cdf-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="23cdf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23cdf-124">Requirements</span></span>



| <span data-ttu-id="23cdf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cdf-125">Requirement</span></span> | <span data-ttu-id="23cdf-126">Value</span><span class="sxs-lookup"><span data-stu-id="23cdf-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23cdf-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23cdf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="23cdf-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="23cdf-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23cdf-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23cdf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="23cdf-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="23cdf-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="23cdf-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="23cdf-131">End of client support</span></span><br/>    | <span data-ttu-id="23cdf-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23cdf-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="23cdf-133">Producto</span><span class="sxs-lookup"><span data-stu-id="23cdf-133">Product</span></span><br/>                  | <span data-ttu-id="23cdf-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="23cdf-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="23cdf-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23cdf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="23cdf-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="23cdf-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="23cdf-137">IID</span><span class="sxs-lookup"><span data-stu-id="23cdf-137">IID</span></span><br/>                      | <span data-ttu-id="23cdf-138">IID \_ IVMSerialPortCollection se define como dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="23cdf-138">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="23cdf-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="23cdf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23cdf-140">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="23cdf-140">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

