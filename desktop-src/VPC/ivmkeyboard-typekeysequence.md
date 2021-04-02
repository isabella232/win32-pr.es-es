---
title: Método IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simula una lista delimitada por comas de las claves que se van a escribir.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Método TypeKeySequence Virtual PC
- Método TypeKeySequence Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997046"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="86008-106">IVMKeyboard:: TypeKeySequence (método)</span><span class="sxs-lookup"><span data-stu-id="86008-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="86008-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86008-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86008-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="86008-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86008-109">Simula una lista delimitada por comas de las claves que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="86008-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="86008-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86008-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="86008-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86008-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86008-112">*keySequence* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86008-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86008-113">Secuencia delimitada por comas de códigos de tecla que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="86008-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86008-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86008-114">Return value</span></span>

<span data-ttu-id="86008-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="86008-115">This method can return one of these values.</span></span>



| <span data-ttu-id="86008-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86008-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="86008-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="86008-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86008-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86008-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="86008-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="86008-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86008-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="86008-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="86008-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="86008-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="86008-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="86008-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="86008-123">La cadena especificada está vacía o contiene un código de clave no válido.</span><span class="sxs-lookup"><span data-stu-id="86008-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="86008-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="86008-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="86008-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="86008-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="86008-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86008-126">Remarks</span></span>

<span data-ttu-id="86008-127">Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación de tecla y de versión de un teclado en estilo estándar 101 de EE. UU..</span><span class="sxs-lookup"><span data-stu-id="86008-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="86008-128">Si aparece un identificador de clave en la cadena sin un modificador anterior, se envía un código presionado con la tecla a la sesión de la máquina virtual, seguido inmediatamente del código de liberación de claves correspondiente.</span><span class="sxs-lookup"><span data-stu-id="86008-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="86008-129">Los modificadores de clave se pueden usar para cambiar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="86008-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="86008-130">Por ejemplo, el modificador DOWN enviará el código presionado por la tecla para el siguiente identificador de clave sin enviar el código liberado por la clave.</span><span class="sxs-lookup"><span data-stu-id="86008-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="86008-131">Esto resulta útil para simular las teclas Ctrl, Alt y Mayús cuando se mantienen presionadas mientras se envían otras claves.</span><span class="sxs-lookup"><span data-stu-id="86008-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="86008-132">Para liberar la clave, se debe volver a incluir en la cadena de clave junto con un modificador anterior.</span><span class="sxs-lookup"><span data-stu-id="86008-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="86008-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86008-133">Requirements</span></span>



| <span data-ttu-id="86008-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="86008-134">Requirement</span></span> | <span data-ttu-id="86008-135">Value</span><span class="sxs-lookup"><span data-stu-id="86008-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86008-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86008-136">Minimum supported client</span></span><br/> | <span data-ttu-id="86008-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="86008-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86008-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86008-138">Minimum supported server</span></span><br/> | <span data-ttu-id="86008-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="86008-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86008-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="86008-140">End of client support</span></span><br/>    | <span data-ttu-id="86008-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86008-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86008-142">Producto</span><span class="sxs-lookup"><span data-stu-id="86008-142">Product</span></span><br/>                  | <span data-ttu-id="86008-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86008-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86008-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86008-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="86008-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="86008-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86008-146">IID</span><span class="sxs-lookup"><span data-stu-id="86008-146">IID</span></span><br/>                      | <span data-ttu-id="86008-147">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="86008-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="86008-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="86008-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86008-149">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="86008-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="86008-150">Secuencias de claves</span><span class="sxs-lookup"><span data-stu-id="86008-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

