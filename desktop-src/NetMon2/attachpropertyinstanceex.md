---
description: La función AttachPropertyInstanceEx asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de la propiedad.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Función AttachPropertyInstanceEx (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677741"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="d4eea-103">AttachPropertyInstanceEx función)</span><span class="sxs-lookup"><span data-stu-id="d4eea-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="d4eea-104">La función **AttachPropertyInstanceEx** asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4eea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4eea-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d4eea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4eea-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-108">Identificador del marco que se está analizando.</span><span class="sxs-lookup"><span data-stu-id="d4eea-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="d4eea-109">Use el identificador que se pasa a la DLL del analizador en el parámetro *hFrame* de la función [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="d4eea-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-110">*hProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-111">Identificador de una estructura [**PROPERTYINFO**](propertyinfo.md) que define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="d4eea-112">Cuando se implementa la función de exportación de [**registro**](register-parser.md) , se especifica la estructura **PROPERTYINFO** que define la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-113">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-114">Longitud de los datos para esta instancia de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-115">*lpData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-116">Puntero a la ubicación de los datos reconocidos donde se encuentra el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="d4eea-117">Use el puntero que se pasa a la DLL del analizador en el parámetro *lpProtocol* de la función [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="d4eea-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-118">*LengthEx* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-119">Longitud de la longitud de los datos extendidos en bytes.</span><span class="sxs-lookup"><span data-stu-id="d4eea-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-120">*lpDataEx* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-121">Puntero a los datos extendidos, que suele ser una variable de pila que contiene los datos de extensión.</span><span class="sxs-lookup"><span data-stu-id="d4eea-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-122">*HelpID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-123">Identificador (de 0 a 2047) que se usa para establecer la ayuda contextual de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="d4eea-124">El número *helpID* es relativo al archivo de ayuda asociado a la [*base de datos de propiedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d4eea-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-125">*IndentLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-126">Nivel de sangría (de 0 a 15) que se usa para mostrar una propiedad jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="d4eea-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="d4eea-127">Monitor de red usa los niveles de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="d4eea-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="d4eea-128">El nivel 15 es un valor especial que permite al analizador adjuntar una propiedad oculta que no está visible.</span><span class="sxs-lookup"><span data-stu-id="d4eea-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="d4eea-129">*IFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4eea-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4eea-130">Un valor de campo de bits que indica el orden de los BITs dentro de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="d4eea-131">Los analizadores anteriores que establecen *fError* en 0 o 1 ahora deberían establecer *fError* en IFLAG \_ error.</span><span class="sxs-lookup"><span data-stu-id="d4eea-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="d4eea-132">Establezca este parámetro en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="d4eea-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="d4eea-133">Value</span><span class="sxs-lookup"><span data-stu-id="d4eea-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d4eea-134">Significado</span><span class="sxs-lookup"><span data-stu-id="d4eea-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="d4eea-135"><dt>**\_error IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="d4eea-136">Los datos del marco tienen un error.</span><span class="sxs-lookup"><span data-stu-id="d4eea-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="d4eea-137"><dt>**IFLAG \_ intercambiada**</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="d4eea-138">En el momento de la asociación, **Word** byte es un formato que no es de Intel.</span><span class="sxs-lookup"><span data-stu-id="d4eea-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="d4eea-139"><dt>**IFLAG \_ UNIcode**</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="d4eea-140">En el momento de la asociación, la **cadena** es Unicode.</span><span class="sxs-lookup"><span data-stu-id="d4eea-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4eea-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4eea-141">Return value</span></span>

<span data-ttu-id="d4eea-142">Si la función se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="d4eea-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="d4eea-143">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="d4eea-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4eea-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4eea-144">Remarks</span></span>

<span data-ttu-id="d4eea-145">Se llama a la función **AttachPropertyInstanceEx** durante la implementación de la función de exportación [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="d4eea-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="d4eea-146">Cuando se adjunta una propiedad a los datos mediante AttachPropertyInstanceEx, Monitor de red crea una estructura [**PROPERTYINST**](propertyinst.md) que define la instancia de la propiedad adjunta y una estructura [**PROPERTYINSTEX**](propertyinstex.md) que define los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="d4eea-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="d4eea-147">Si se llama a **AttachPropertyInstanceEx** y no se proporcionan datos extendidos, el parámetro *lpDataEx* es **null** o el parámetro *LengthEx* es 0, la llamada **AttachPropertyInstanceEx** es funcionalmente equivalente a una llamada [**AttachPropertyInstance**](attachpropertyinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="d4eea-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="d4eea-148">Durante la implementación de [**AttachProperties**](attachproperties.md), llame a [**AttachPropertyInstance**](attachpropertyinstance.md) para usar los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="d4eea-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="d4eea-149">También puede llamar a la función **AttachPropertyInstanceEx** para modificar los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4eea-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="d4eea-150">Sin embargo, se recomienda que use los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="d4eea-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4eea-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4eea-151">Requirements</span></span>



| <span data-ttu-id="d4eea-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4eea-152">Requirement</span></span> | <span data-ttu-id="d4eea-153">Value</span><span class="sxs-lookup"><span data-stu-id="d4eea-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4eea-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4eea-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d4eea-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4eea-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d4eea-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4eea-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d4eea-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4eea-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4eea-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4eea-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4eea-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d4eea-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4eea-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4eea-161"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4eea-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4eea-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4eea-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4eea-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




