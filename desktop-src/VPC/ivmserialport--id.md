---
title: Método _ID IVMSerialPort (VPCCOMInterfaces. h)
description: Identificador interno del puerto serie.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID método virtual PC
- Método _ID Virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, método _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150249"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="f0398-106">IVMSerialPort:: \_ ID (método)</span><span class="sxs-lookup"><span data-stu-id="f0398-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="f0398-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0398-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0398-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0398-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0398-109">Recupera el identificador interno del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="f0398-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0398-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0398-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="f0398-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0398-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0398-112">*portID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0398-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0398-113">Identificador del puerto serie.</span><span class="sxs-lookup"><span data-stu-id="f0398-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0398-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0398-114">Return value</span></span>

<span data-ttu-id="f0398-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f0398-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f0398-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0398-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="f0398-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0398-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0398-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0398-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f0398-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0398-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f0398-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0398-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f0398-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f0398-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="f0398-122"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0398-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f0398-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f0398-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="f0398-124"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f0398-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f0398-125">La configuración de esta máquina virtual no es válida.</span><span class="sxs-lookup"><span data-stu-id="f0398-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0398-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0398-126">Remarks</span></span>

<span data-ttu-id="f0398-127">Esta propiedad no se puede usar en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="f0398-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0398-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0398-128">Requirements</span></span>



| <span data-ttu-id="f0398-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0398-129">Requirement</span></span> | <span data-ttu-id="f0398-130">Value</span><span class="sxs-lookup"><span data-stu-id="f0398-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0398-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0398-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f0398-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0398-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0398-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0398-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f0398-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0398-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0398-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f0398-135">End of client support</span></span><br/>    | <span data-ttu-id="f0398-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0398-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0398-137">Producto</span><span class="sxs-lookup"><span data-stu-id="f0398-137">Product</span></span><br/>                  | <span data-ttu-id="f0398-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0398-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0398-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0398-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0398-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0398-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0398-141">IID</span><span class="sxs-lookup"><span data-stu-id="f0398-141">IID</span></span><br/>                      | <span data-ttu-id="f0398-142">IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="f0398-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f0398-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0398-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0398-144">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f0398-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

