---
title: Propiedad del elemento IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de conexión del disco duro correspondiente al índice especificado.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMHardDiskConnectionCollection
- Interfaz IVMHardDiskConnectionCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676551"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a><span data-ttu-id="3d5bf-106">IVMHardDiskConnectionCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3d5bf-106">IVMHardDiskConnectionCollection::Item property</span></span>

<span data-ttu-id="3d5bf-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d5bf-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d5bf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d5bf-109">Recupera el objeto de conexión del disco duro correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-109">Retrieves the hard disk connection object that corresponds to the specified index.</span></span>

<span data-ttu-id="3d5bf-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5bf-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d5bf-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a><span data-ttu-id="3d5bf-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3d5bf-112">Property value</span></span>

<span data-ttu-id="3d5bf-113">El objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="3d5bf-113">The [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d5bf-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3d5bf-114">Error codes</span></span>



| <span data-ttu-id="3d5bf-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3d5bf-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3d5bf-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3d5bf-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d5bf-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3d5bf-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="3d5bf-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3d5bf-120">El parámetro *hardDiskConnection* es **null**.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-120">The *hardDiskConnection* parameter is **NULL**.</span></span> <br/>                                    |
| <dl> <span data-ttu-id="3d5bf-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="3d5bf-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="3d5bf-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3d5bf-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="3d5bf-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3d5bf-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3d5bf-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="3d5bf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d5bf-127">Requirements</span></span>



| <span data-ttu-id="3d5bf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d5bf-128">Requirement</span></span> | <span data-ttu-id="3d5bf-129">Value</span><span class="sxs-lookup"><span data-stu-id="3d5bf-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5bf-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d5bf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5bf-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d5bf-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="3d5bf-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d5bf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5bf-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3d5bf-133">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="3d5bf-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3d5bf-134">End of client support</span></span><br/>    | <span data-ttu-id="3d5bf-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d5bf-135">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="3d5bf-136">Producto</span><span class="sxs-lookup"><span data-stu-id="3d5bf-136">Product</span></span><br/>                  | <span data-ttu-id="3d5bf-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d5bf-137">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="3d5bf-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d5bf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5bf-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bf-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="3d5bf-140">IID</span><span class="sxs-lookup"><span data-stu-id="3d5bf-140">IID</span></span><br/>                      | <span data-ttu-id="3d5bf-141">IID \_ IVMHardDiskconnectionCollection se define como b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="3d5bf-141">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d5bf-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d5bf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5bf-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="3d5bf-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="3d5bf-144">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="3d5bf-144">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

