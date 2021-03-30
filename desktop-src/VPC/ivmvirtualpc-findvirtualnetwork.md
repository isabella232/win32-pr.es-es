---
title: Método IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera un objeto de red virtual que coincide con el nombre solicitado.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Método FindVirtualNetwork Virtual PC
- Método FindVirtualNetwork Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534857"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="a16b8-106">IVMVirtualPC:: FindVirtualNetwork (método)</span><span class="sxs-lookup"><span data-stu-id="a16b8-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="a16b8-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a16b8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a16b8-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a16b8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a16b8-109">Recupera un objeto de red virtual que coincide con el nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="a16b8-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16b8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a16b8-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="a16b8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a16b8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16b8-112">*virtualNetworkName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a16b8-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a16b8-113">Nombre de la red virtual que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a16b8-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="a16b8-114">*virtualNetwork* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a16b8-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a16b8-115">Un puntero a un nuevo objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa esta red virtual.</span><span class="sxs-lookup"><span data-stu-id="a16b8-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16b8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a16b8-116">Return value</span></span>

<span data-ttu-id="a16b8-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a16b8-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a16b8-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a16b8-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="a16b8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a16b8-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a16b8-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="a16b8-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a16b8-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a16b8-122"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="a16b8-123">No se encontró la red virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="a16b8-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a16b8-124"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="a16b8-125">El parámetro *virtualNetwork* es **null** o no se encuentra la red virtual.</span><span class="sxs-lookup"><span data-stu-id="a16b8-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="a16b8-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="a16b8-127">El parámetro *virtualNetworkName* no es válido o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a16b8-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="a16b8-128"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="a16b8-129">No se encontró el archivo de red virtual.</span><span class="sxs-lookup"><span data-stu-id="a16b8-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a16b8-130"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="a16b8-131">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a16b8-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a16b8-132"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="a16b8-133">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="a16b8-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a16b8-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a16b8-134">Remarks</span></span>

<span data-ttu-id="a16b8-135">Los nombres de red virtual no distinguen mayúsculas de minúsculas, por ejemplo, "subred" y "subred" hacen referencia a la misma red virtual.</span><span class="sxs-lookup"><span data-stu-id="a16b8-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16b8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a16b8-136">Requirements</span></span>



| <span data-ttu-id="a16b8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16b8-137">Requirement</span></span> | <span data-ttu-id="a16b8-138">Value</span><span class="sxs-lookup"><span data-stu-id="a16b8-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a16b8-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16b8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a16b8-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a16b8-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a16b8-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a16b8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a16b8-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a16b8-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a16b8-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a16b8-143">End of client support</span></span><br/>    | <span data-ttu-id="a16b8-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a16b8-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a16b8-145">Producto</span><span class="sxs-lookup"><span data-stu-id="a16b8-145">Product</span></span><br/>                  | <span data-ttu-id="a16b8-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a16b8-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a16b8-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a16b8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a16b8-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16b8-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a16b8-149">IID</span><span class="sxs-lookup"><span data-stu-id="a16b8-149">IID</span></span><br/>                      | <span data-ttu-id="a16b8-150">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a16b8-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a16b8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a16b8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16b8-152">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a16b8-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

