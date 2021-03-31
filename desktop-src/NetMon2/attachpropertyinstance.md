---
description: La función AttachPropertyInstance asigna una propiedad existente a una ubicación específica en los datos reconocidos.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: Función AttachPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911649"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="cb46a-103">AttachPropertyInstance función)</span><span class="sxs-lookup"><span data-stu-id="cb46a-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="cb46a-104">La función **AttachPropertyInstance** asigna una propiedad existente a una ubicación específica en los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="cb46a-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb46a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb46a-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cb46a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb46a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb46a-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-108">Identificador del marco que se está analizando.</span><span class="sxs-lookup"><span data-stu-id="cb46a-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="cb46a-109">Use el identificador que se pasa a la DLL del analizador en el parámetro *hFrame* de la función [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="cb46a-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-110">*hProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-111">Identificador de una estructura [**PROPERTYINFO**](propertyinfo.md) que define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="cb46a-112">Cuando se implementa la función de exportación de [**registro**](register-parser.md) , se especifica la estructura **PROPERTYINFO** que define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-113">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-114">Longitud de los datos para esta instancia de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-115">*lpData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-116">Puntero a la ubicación de los datos reconocidos donde se encuentra el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="cb46a-117">Use el puntero que se pasa a la DLL del analizador en el parámetro *lpProtocol* de la función [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="cb46a-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-118">*HelpID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-119">Identificador (de 0 a 2047) que se usa para establecer la ayuda contextual para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="cb46a-120">El número de identificación es relativo al archivo de ayuda asociado a la [*base de datos de propiedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cb46a-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-121">*IndentLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-122">Nivel de sangría (de 0 a 15) que se usa para mostrar una propiedad jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="cb46a-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="cb46a-123">Monitor de red usa los niveles 0 a 14 para aplicar sangría a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb46a-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="cb46a-124">El nivel 15 es un valor especial que permite a un analizador adjuntar una propiedad oculta que no está visible.</span><span class="sxs-lookup"><span data-stu-id="cb46a-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="cb46a-125">*IFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb46a-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46a-126">Un valor de campo de bits que indica el orden de los BITs dentro de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="cb46a-127">Los analizadores anteriores que establecen *fError* en 0 o 1 ahora deberían establecer *fError* en IFLAG \_ error.</span><span class="sxs-lookup"><span data-stu-id="cb46a-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="cb46a-128">Establezca este parámetro en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="cb46a-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="cb46a-129">Value</span><span class="sxs-lookup"><span data-stu-id="cb46a-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="cb46a-130">Significado</span><span class="sxs-lookup"><span data-stu-id="cb46a-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="cb46a-131"><dt>**\_error IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="cb46a-132">Los datos del marco tienen un error.</span><span class="sxs-lookup"><span data-stu-id="cb46a-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="cb46a-133"><dt>**IFLAG \_ intercambiada**</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="cb46a-134">En el momento de la asociación, **Word** byte es un formato que no es de Intel.</span><span class="sxs-lookup"><span data-stu-id="cb46a-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="cb46a-135"><dt>**IFLAG \_ UNIcode**</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="cb46a-136">En el momento de la asociación, la **cadena** es Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb46a-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb46a-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb46a-137">Return value</span></span>

<span data-ttu-id="cb46a-138">Si la función se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="cb46a-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="cb46a-139">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="cb46a-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb46a-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb46a-140">Remarks</span></span>

<span data-ttu-id="cb46a-141">Se llama a la función **AttachPropertyInstance** durante la implementación de la función de exportación [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="cb46a-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="cb46a-142">Cuando se adjunta una propiedad a los datos, Monitor de red crea una estructura [**PROPERTYINST**](propertyinst.md) que define la instancia de la propiedad adjunta.</span><span class="sxs-lookup"><span data-stu-id="cb46a-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="cb46a-143">Durante la implementación de [**AttachProperties**](attachproperties.md), llame a **AttachPropertyInstance** para usar los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="cb46a-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="cb46a-144">También puede llamar a la función [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para modificar los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cb46a-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="cb46a-145">Sin embargo, se recomienda que use los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="cb46a-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="cb46a-146">Para obtener información sobre</span><span class="sxs-lookup"><span data-stu-id="cb46a-146">For Information on</span></span>                                        | <span data-ttu-id="cb46a-147">Vea</span><span class="sxs-lookup"><span data-stu-id="cb46a-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cb46a-148">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="cb46a-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="cb46a-149">**Analizadores**</span><span class="sxs-lookup"><span data-stu-id="cb46a-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="cb46a-150">Cómo llamar a **AttachPropertyInstance**.</span><span class="sxs-lookup"><span data-stu-id="cb46a-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="cb46a-151">Implementación de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="cb46a-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="cb46a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb46a-152">Requirements</span></span>



| <span data-ttu-id="cb46a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb46a-153">Requirement</span></span> | <span data-ttu-id="cb46a-154">Value</span><span class="sxs-lookup"><span data-stu-id="cb46a-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb46a-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb46a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cb46a-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cb46a-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cb46a-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb46a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cb46a-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb46a-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb46a-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb46a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb46a-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cb46a-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb46a-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb46a-162"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb46a-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb46a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb46a-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb46a-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb46a-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb46a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb46a-166">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="cb46a-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="cb46a-167">**AttachPropertyInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="cb46a-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="cb46a-168">**PROPERTYINST**</span><span class="sxs-lookup"><span data-stu-id="cb46a-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




