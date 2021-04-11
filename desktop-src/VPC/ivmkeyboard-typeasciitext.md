---
title: Método IVMKeyboard TypeAsciiText (VPCCOMInterfaces. h)
description: Simula una serie de claves ASCII que se escriben en el invitado.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Método TypeAsciiText Virtual PC
- Método TypeAsciiText Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método TypeAsciiText
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150483"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="0d3cc-106">IVMKeyboard:: TypeAsciiText (método)</span><span class="sxs-lookup"><span data-stu-id="0d3cc-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="0d3cc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d3cc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d3cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d3cc-109">Simula una serie de claves ASCII que se escriben en el invitado.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3cc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d3cc-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="0d3cc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d3cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3cc-112">*texto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0d3cc-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3cc-113">Cadena de texto ASCII que se va a escribir dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3cc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d3cc-114">Return value</span></span>

<span data-ttu-id="0d3cc-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0d3cc-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d3cc-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="0d3cc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d3cc-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0d3cc-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cc-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0d3cc-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0d3cc-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cc-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0d3cc-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0d3cc-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cc-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="0d3cc-123">La cadena especificada está vacía.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="0d3cc-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cc-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0d3cc-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0d3cc-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d3cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3cc-126">Requirements</span></span>



| <span data-ttu-id="0d3cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3cc-127">Requirement</span></span> | <span data-ttu-id="0d3cc-128">Value</span><span class="sxs-lookup"><span data-stu-id="0d3cc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3cc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3cc-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d3cc-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d3cc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3cc-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0d3cc-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d3cc-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0d3cc-133">End of client support</span></span><br/>    | <span data-ttu-id="0d3cc-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d3cc-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d3cc-135">Producto</span><span class="sxs-lookup"><span data-stu-id="0d3cc-135">Product</span></span><br/>                  | <span data-ttu-id="0d3cc-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d3cc-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d3cc-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d3cc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d3cc-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cc-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d3cc-139">IID</span><span class="sxs-lookup"><span data-stu-id="0d3cc-139">IID</span></span><br/>                      | <span data-ttu-id="0d3cc-140">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="0d3cc-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0d3cc-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3cc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3cc-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="0d3cc-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

