---
title: Método IsPressed IVMKeyboard (VPCCOMInterfaces. h)
description: Determina si la tecla especificada está presionada.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- IsPressed (método, equipo virtual PC)
- Método IsPressed Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método IsPressed
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803098"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="84f53-106">IVMKeyboard:: IsPressed (método)</span><span class="sxs-lookup"><span data-stu-id="84f53-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="84f53-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84f53-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84f53-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84f53-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84f53-109">Determina si la tecla especificada está presionada.</span><span class="sxs-lookup"><span data-stu-id="84f53-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f53-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84f53-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="84f53-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84f53-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f53-112">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="84f53-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f53-113">Código clave de la clave cuyo estado se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="84f53-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="84f53-114">*presionado* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="84f53-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="84f53-115">**True** si la tecla está presionada actualmente, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="84f53-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f53-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84f53-116">Return value</span></span>

<span data-ttu-id="84f53-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="84f53-117">This method can return one of these values.</span></span>



| <span data-ttu-id="84f53-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84f53-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="84f53-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="84f53-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84f53-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84f53-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="84f53-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="84f53-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="84f53-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="84f53-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="84f53-123">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="84f53-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="84f53-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="84f53-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="84f53-125">La cadena especificada está vacía o contiene un código de clave no válido.</span><span class="sxs-lookup"><span data-stu-id="84f53-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="84f53-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="84f53-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="84f53-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="84f53-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="84f53-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f53-128">Requirements</span></span>



| <span data-ttu-id="84f53-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f53-129">Requirement</span></span> | <span data-ttu-id="84f53-130">Value</span><span class="sxs-lookup"><span data-stu-id="84f53-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f53-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84f53-131">Minimum supported client</span></span><br/> | <span data-ttu-id="84f53-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="84f53-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f53-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84f53-133">Minimum supported server</span></span><br/> | <span data-ttu-id="84f53-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="84f53-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84f53-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="84f53-135">End of client support</span></span><br/>    | <span data-ttu-id="84f53-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84f53-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84f53-137">Producto</span><span class="sxs-lookup"><span data-stu-id="84f53-137">Product</span></span><br/>                  | <span data-ttu-id="84f53-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84f53-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84f53-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84f53-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f53-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f53-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84f53-141">IID</span><span class="sxs-lookup"><span data-stu-id="84f53-141">IID</span></span><br/>                      | <span data-ttu-id="84f53-142">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="84f53-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="84f53-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="84f53-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f53-144">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="84f53-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

