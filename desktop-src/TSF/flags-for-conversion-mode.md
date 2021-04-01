---
title: Marcas para el modo de conversión (Ctffunc. h)
description: Las marcas siguientes se usan como un valor de conversión de INPUTMODE de teclado del compartimiento de GUID \_ \_ \_ \_ . Esto es equivalente a \_ los valores de CMODE de IME para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Marcas para el marco de trabajo de servicios de texto en modo de conversión
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150433"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="add8b-105">Marcas para el modo de conversión</span><span class="sxs-lookup"><span data-stu-id="add8b-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="add8b-106">Las marcas siguientes se usan como un valor de [ \_ conversión de \_ \_ INPUTMODE \_ de teclado del compartimiento de GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="add8b-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="add8b-107">Esto es equivalente a los valores de [ \_ CMODE de IME](../intl/ime-conversion-mode-values.md) para IMM32.</span><span class="sxs-lookup"><span data-stu-id="add8b-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="add8b-108">Marca</span><span class="sxs-lookup"><span data-stu-id="add8b-108">Flag</span></span>                             | <span data-ttu-id="add8b-109">Value</span><span class="sxs-lookup"><span data-stu-id="add8b-109">Value</span></span>  | <span data-ttu-id="add8b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="add8b-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="add8b-111">TF \_ CONVERSIONMODE \_ alfanumérico</span><span class="sxs-lookup"><span data-stu-id="add8b-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="add8b-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="add8b-112">0x0000</span></span> | <span data-ttu-id="add8b-113">Se establece en 1 si el modo alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="add8b-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="add8b-114">TF \_ CONVERSIONMODE \_ Native</span><span class="sxs-lookup"><span data-stu-id="add8b-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="add8b-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="add8b-115">0x0001</span></span> | <span data-ttu-id="add8b-116">Se establece en 1 si el modo nativo; 0 si el modo es alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="add8b-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="add8b-117">TF \_ CONVERSIONMODE \_ katakana</span><span class="sxs-lookup"><span data-stu-id="add8b-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="add8b-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="add8b-118">0x0002</span></span> | <span data-ttu-id="add8b-119">Se establece en 1 si el modo KATAKANA; 0 si el modo es HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="add8b-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="add8b-120">TF \_ CONVERSIONMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="add8b-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="add8b-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="add8b-121">0x0008</span></span> | <span data-ttu-id="add8b-122">Se establece en 1 si el modo de forma completa; 0 si el modo de mitad de la forma.</span><span class="sxs-lookup"><span data-stu-id="add8b-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="add8b-123">TF \_ CONVERSIONMODE \_ Roman</span><span class="sxs-lookup"><span data-stu-id="add8b-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="add8b-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="add8b-124">0x0010</span></span> | <span data-ttu-id="add8b-125">Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="add8b-126">\_CONVERSIONMODE \_ CódCar</span><span class="sxs-lookup"><span data-stu-id="add8b-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="add8b-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="add8b-127">0x0020</span></span> | <span data-ttu-id="add8b-128">Se establece en 1 si el modo de entrada del código de carácter; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="add8b-129">TF \_ CONVERSIONMODE \_ SOFTKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="add8b-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="add8b-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="add8b-130">0x0080</span></span> | <span data-ttu-id="add8b-131">Se establece en 1 si el modo de teclado en pantalla; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="add8b-132">TF \_ CONVERSIONMODE \_ Conversion</span><span class="sxs-lookup"><span data-stu-id="add8b-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="add8b-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="add8b-133">0x0100</span></span> | <span data-ttu-id="add8b-134">Se establece en 1 para evitar el procesamiento de conversiones por parte de IME; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="add8b-135">símbolo de TF \_ CONVERSIONMODE \_</span><span class="sxs-lookup"><span data-stu-id="add8b-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="add8b-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="add8b-136">0x0400</span></span> | <span data-ttu-id="add8b-137">Se establece en 1 si el modo de conversión de símbolos; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="add8b-138">TF \_ CONVERSIONMODE \_ fixed</span><span class="sxs-lookup"><span data-stu-id="add8b-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="add8b-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="add8b-139">0x0800</span></span> | <span data-ttu-id="add8b-140">Se establece en 1 si el modo de conversión es fijo; 0 si no es así.</span><span class="sxs-lookup"><span data-stu-id="add8b-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="add8b-141">Los valores siguientes se usan como un valor de [ \_ INPUTMODE de \_ teclado \_ \_ de compartimiento de GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="add8b-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="add8b-142">Esto es equivalente a los valores de [ \_ SMODE de IME](../intl/ime-composition-string-values.md) para IMM32.</span><span class="sxs-lookup"><span data-stu-id="add8b-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="add8b-143">Marca</span><span class="sxs-lookup"><span data-stu-id="add8b-143">Flag</span></span>                            | <span data-ttu-id="add8b-144">Value</span><span class="sxs-lookup"><span data-stu-id="add8b-144">Value</span></span>  | <span data-ttu-id="add8b-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="add8b-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="add8b-146">TF \_ SENTENCEMODE \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="add8b-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="add8b-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="add8b-147">0x0000</span></span> | <span data-ttu-id="add8b-148">No hay información para la frase.</span><span class="sxs-lookup"><span data-stu-id="add8b-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="add8b-149">TF \_ SENTENCEMODE \_ PLAURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="add8b-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="add8b-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="add8b-150">0x0001</span></span> | <span data-ttu-id="add8b-151">El IME usa la información de la cláusula plural para llevar a cabo el procesamiento de la conversión.</span><span class="sxs-lookup"><span data-stu-id="add8b-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="add8b-152">TF \_ SENTENCEMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="add8b-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="add8b-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="add8b-153">0x0002</span></span> | <span data-ttu-id="add8b-154">El IME realiza el procesamiento de la conversión en el modo de un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="add8b-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="add8b-155">TF \_ SENTENCEMODE \_ Automatic</span><span class="sxs-lookup"><span data-stu-id="add8b-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="add8b-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="add8b-156">0x0004</span></span> | <span data-ttu-id="add8b-157">El IME realiza el procesamiento de la conversión en modo automático.</span><span class="sxs-lookup"><span data-stu-id="add8b-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="add8b-158">TF \_ SENTENCEMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="add8b-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="add8b-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="add8b-159">0x0008</span></span> | <span data-ttu-id="add8b-160">El IME usa la información de frases para predecir el siguiente carácter.</span><span class="sxs-lookup"><span data-stu-id="add8b-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="add8b-161">TF \_ SENTENCEMODE \_ Conversation</span><span class="sxs-lookup"><span data-stu-id="add8b-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="add8b-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="add8b-162">0x0010</span></span> | <span data-ttu-id="add8b-163">El IME usa el modo de conversación.</span><span class="sxs-lookup"><span data-stu-id="add8b-163">The IME uses conversation mode.</span></span> <span data-ttu-id="add8b-164">Esto resulta útil para las aplicaciones de chat.</span><span class="sxs-lookup"><span data-stu-id="add8b-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="add8b-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add8b-165">Requirements</span></span>



| <span data-ttu-id="add8b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="add8b-166">Requirement</span></span> | <span data-ttu-id="add8b-167">Value</span><span class="sxs-lookup"><span data-stu-id="add8b-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="add8b-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="add8b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="add8b-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="add8b-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="add8b-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="add8b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="add8b-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="add8b-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="add8b-172">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="add8b-172">Redistributable</span></span><br/>          | <span data-ttu-id="add8b-173">TSF 1,0 Windows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98</span><span class="sxs-lookup"><span data-stu-id="add8b-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="add8b-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="add8b-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="add8b-175"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="add8b-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="add8b-176">IDL</span><span class="sxs-lookup"><span data-stu-id="add8b-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="add8b-177"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="add8b-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add8b-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="add8b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add8b-179">Compartimientos predefinidos</span><span class="sxs-lookup"><span data-stu-id="add8b-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

