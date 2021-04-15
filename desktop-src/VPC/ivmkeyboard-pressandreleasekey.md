---
title: Método IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simula que se presiona una tecla y luego se libera.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Método PressAndReleaseKey Virtual PC
- Método PressAndReleaseKey Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695961"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="6a37e-106">IVMKeyboard::P método ressAndReleaseKey</span><span class="sxs-lookup"><span data-stu-id="6a37e-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="6a37e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6a37e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6a37e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6a37e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6a37e-109">Simula que se presiona una tecla y luego se libera.</span><span class="sxs-lookup"><span data-stu-id="6a37e-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a37e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a37e-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="6a37e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a37e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a37e-112">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6a37e-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a37e-113">Código clave de la tecla que se va a presionar y liberar.</span><span class="sxs-lookup"><span data-stu-id="6a37e-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a37e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a37e-114">Return value</span></span>

<span data-ttu-id="6a37e-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6a37e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6a37e-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a37e-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="6a37e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a37e-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a37e-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6a37e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6a37e-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a37e-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6a37e-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6a37e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6a37e-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="6a37e-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6a37e-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6a37e-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="6a37e-123">La cadena especificada está vacía o contiene un código de clave no válido.</span><span class="sxs-lookup"><span data-stu-id="6a37e-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="6a37e-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6a37e-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6a37e-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="6a37e-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="6a37e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a37e-126">Requirements</span></span>



| <span data-ttu-id="6a37e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a37e-127">Requirement</span></span> | <span data-ttu-id="6a37e-128">Value</span><span class="sxs-lookup"><span data-stu-id="6a37e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a37e-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a37e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a37e-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a37e-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6a37e-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a37e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a37e-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6a37e-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6a37e-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6a37e-133">End of client support</span></span><br/>    | <span data-ttu-id="6a37e-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a37e-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6a37e-135">Producto</span><span class="sxs-lookup"><span data-stu-id="6a37e-135">Product</span></span><br/>                  | <span data-ttu-id="6a37e-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6a37e-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6a37e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a37e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a37e-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a37e-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6a37e-139">IID</span><span class="sxs-lookup"><span data-stu-id="6a37e-139">IID</span></span><br/>                      | <span data-ttu-id="6a37e-140">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="6a37e-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6a37e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a37e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a37e-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="6a37e-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

