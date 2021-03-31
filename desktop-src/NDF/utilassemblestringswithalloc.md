---
title: Función UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Asigna una cadena y le da formato mediante las cadenas proporcionadas por la tabla de cadenas. Esta función usa StringCchPrintf para crear la cadena con formato.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc función NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804063"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="af59a-105">UtilAssembleStringsWithAlloc función)</span><span class="sxs-lookup"><span data-stu-id="af59a-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="af59a-106">La función **UtilAssembleStringsWithAlloc** asigna una cadena y le da formato mediante las cadenas proporcionadas por la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="af59a-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="af59a-107">Esta función usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) para crear la cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="af59a-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="af59a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af59a-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="af59a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af59a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af59a-110">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af59a-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-111">Tipo: \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="af59a-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="af59a-112">Ubicación donde se colocará la cadena recién asignada.</span><span class="sxs-lookup"><span data-stu-id="af59a-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="af59a-113">Cuando la cadena ya no es necesaria, se debe liberar con [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="af59a-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="af59a-114">*BufferMax* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af59a-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="af59a-115">Type: **UINT**</span></span>

<span data-ttu-id="af59a-116">Número máximo de caracteres permitidos en la cadena asignada por el *búfer*.</span><span class="sxs-lookup"><span data-stu-id="af59a-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="af59a-117">Si la cadena con formato resultante es mayor que el número de caracteres especificado, se trunca y termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="af59a-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="af59a-118">Este parámetro no se puede establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="af59a-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="af59a-119">*Formatodeentrada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af59a-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="af59a-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="af59a-121">Recurso de cadena fuera de la tabla de cadenas que representa un parámetro de formato pasado a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span><span class="sxs-lookup"><span data-stu-id="af59a-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="af59a-122">Se construye mediante [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="af59a-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="af59a-123">El formato de la cadena de recursos debe especificar un parámetro de formato que toma una cadena de caracteres anchos, o un parámetro de formato que toma una longitud sin signo y una cadena de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="af59a-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="af59a-124">*InputString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af59a-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-125">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="af59a-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="af59a-126">Recurso de cadena fuera de la tabla de cadenas que representa un argumento pasado a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) en lugar de la cadena ancha en el parámetro Format.</span><span class="sxs-lookup"><span data-stu-id="af59a-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="af59a-127">Se construye mediante [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="af59a-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="af59a-128">*AdditionalArgument* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af59a-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-129">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="af59a-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="af59a-130">True si *AdditionalValue* debe pasarse como el primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); de lo contrario, es false (y solo se pasará la cadena de recursos identificada por *InputString* ).</span><span class="sxs-lookup"><span data-stu-id="af59a-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="af59a-131">*AdditionalValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af59a-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af59a-132">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="af59a-132">Type: **ULONG**</span></span>

<span data-ttu-id="af59a-133">Valor que se va a pasar como primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) si *AdditionalArgument* es true.</span><span class="sxs-lookup"><span data-stu-id="af59a-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af59a-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af59a-134">Return value</span></span>

<span data-ttu-id="af59a-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="af59a-135">Type: **HRESULT**</span></span>

<span data-ttu-id="af59a-136">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="af59a-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="af59a-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="af59a-137">Return code</span></span>                                                                                  | <span data-ttu-id="af59a-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="af59a-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="af59a-139"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="af59a-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="af59a-140">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="af59a-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="af59a-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af59a-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="af59a-142">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="af59a-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="af59a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af59a-143">Requirements</span></span>



| <span data-ttu-id="af59a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="af59a-144">Requirement</span></span> | <span data-ttu-id="af59a-145">Value</span><span class="sxs-lookup"><span data-stu-id="af59a-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="af59a-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af59a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="af59a-147">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="af59a-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af59a-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af59a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="af59a-149">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="af59a-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="af59a-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af59a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="af59a-151"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="af59a-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af59a-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="af59a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af59a-153">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="af59a-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="af59a-154">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="af59a-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="af59a-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="af59a-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="af59a-156">**MAKEINTRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="af59a-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="af59a-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="af59a-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

