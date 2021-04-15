---
title: Propiedad del elemento IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de puerto serie que corresponde al índice especificado.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMSerialPortCollection
- Interfaz IVMSerialPortCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695955"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="f16f3-106">IVMSerialPortCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f16f3-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="f16f3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f16f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f16f3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f16f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f16f3-109">Recupera el objeto de puerto serie que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="f16f3-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="f16f3-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f16f3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16f3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f16f3-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="f16f3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f16f3-112">Property value</span></span>

<span data-ttu-id="f16f3-113">El objeto [**IVMSerialPort**](ivmserialport.md) .</span><span class="sxs-lookup"><span data-stu-id="f16f3-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f16f3-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f16f3-114">Error codes</span></span>



| <span data-ttu-id="f16f3-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f16f3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f16f3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f16f3-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f16f3-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f16f3-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f16f3-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="f16f3-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f16f3-120">El parámetro *serialPort* es NULL.</span><span class="sxs-lookup"><span data-stu-id="f16f3-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="f16f3-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="f16f3-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f16f3-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="f16f3-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f16f3-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="f16f3-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f16f3-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f16f3-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f16f3-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="f16f3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16f3-127">Requirements</span></span>



| <span data-ttu-id="f16f3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16f3-128">Requirement</span></span> | <span data-ttu-id="f16f3-129">Value</span><span class="sxs-lookup"><span data-stu-id="f16f3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16f3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f16f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f16f3-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f16f3-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f16f3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f16f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f16f3-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f16f3-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f16f3-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f16f3-134">End of client support</span></span><br/>    | <span data-ttu-id="f16f3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f16f3-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f16f3-136">Producto</span><span class="sxs-lookup"><span data-stu-id="f16f3-136">Product</span></span><br/>                  | <span data-ttu-id="f16f3-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f16f3-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f16f3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f16f3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16f3-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16f3-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f16f3-140">IID</span><span class="sxs-lookup"><span data-stu-id="f16f3-140">IID</span></span><br/>                      | <span data-ttu-id="f16f3-141">IID \_ IVMSerialPortCollection se define como dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="f16f3-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="f16f3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f16f3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16f3-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f16f3-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="f16f3-144">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="f16f3-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

