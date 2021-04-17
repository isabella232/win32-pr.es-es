---
description: La función de exportación AttachProperties asigna las propiedades a una ubicación dentro de una parte de datos reconocidos. AttachProperties debe implementarse para cada analizador que admita el archivo DLL del analizador.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Función de devolución de llamada AttachProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677740"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="adb18-104">Función de devolución de llamada AttachProperties</span><span class="sxs-lookup"><span data-stu-id="adb18-104">AttachProperties callback function</span></span>

<span data-ttu-id="adb18-105">La función de exportación **AttachProperties** asigna las propiedades a una ubicación dentro de una parte de datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="adb18-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="adb18-106">**AttachProperties** debe implementarse para cada analizador que admita el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="adb18-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb18-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adb18-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="adb18-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adb18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb18-109">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-110">Identificador del marco que se está analizando.</span><span class="sxs-lookup"><span data-stu-id="adb18-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-111">*lpFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-112">Puntero al primer byte de un marco.</span><span class="sxs-lookup"><span data-stu-id="adb18-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-113">*lpProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-114">Puntero al principio de los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="adb18-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-115">*MacType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-116">Valor MAC del primer protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="adb18-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="adb18-117">*MacType* puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="adb18-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="adb18-118">Value</span><span class="sxs-lookup"><span data-stu-id="adb18-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="adb18-119">Significado</span><span class="sxs-lookup"><span data-stu-id="adb18-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="adb18-120"><dt>**\_Ethernet de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="adb18-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="adb18-121">802.3</span><span class="sxs-lookup"><span data-stu-id="adb18-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="adb18-122"><dt>**\_TOKENRING de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="adb18-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="adb18-123">802.5</span><span class="sxs-lookup"><span data-stu-id="adb18-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="adb18-124"><dt>**\_FDDI de tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="adb18-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="adb18-125">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="adb18-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="adb18-126">*BytesLeft* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-127">El número restante de bytes en un marco que empieza al principio de los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="adb18-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-128">*hPreviousProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-129">Identificador del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="adb18-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-130">*nPreviousProtocolOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-131">Desplazamiento del protocolo anterior a partir del principio del marco.</span><span class="sxs-lookup"><span data-stu-id="adb18-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="adb18-132">*lpInstData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="adb18-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb18-133">Puntero a los datos de instancia proporcionados por el protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="adb18-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="adb18-134">Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.</span><span class="sxs-lookup"><span data-stu-id="adb18-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb18-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adb18-135">Return value</span></span>

<span data-ttu-id="adb18-136">Si la función es correcta, el valor devuelto es un puntero al primer byte después de los datos reconocidos en un marco o **null** si los datos reconocidos son la última parte de los datos de un marco.</span><span class="sxs-lookup"><span data-stu-id="adb18-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="adb18-137">Si la función no es correcta, el valor devuelto es un puntero a los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="adb18-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="adb18-138">El parámetro *lpProtocol* pasa el puntero a la dll del analizador.</span><span class="sxs-lookup"><span data-stu-id="adb18-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="adb18-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="adb18-139">Remarks</span></span>

<span data-ttu-id="adb18-140">Monitor de red llama a la función **AttachProperties** para cada analizador que reconoce un fragmento de datos en un marco.</span><span class="sxs-lookup"><span data-stu-id="adb18-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="adb18-141">Tenga en cuenta que el analizador determina qué propiedades existen en los datos reconocidos y dónde se encuentra cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="adb18-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="adb18-142">Durante la implementación de **AttachProperties**, llame a [AttachPropertyInstance](attachpropertyinstance.md) para usar los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="adb18-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="adb18-143">También puede llamar a la función [AttachPropertyInstanceEx](attachpropertyinstanceex.md) para modificar los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="adb18-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="adb18-144">Sin embargo, se recomienda que use los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="adb18-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="adb18-145">Solo se llama a las funciones **AttachPropertyInstanceEx** y **AttachPropertyInstance** para las propiedades que existen en los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="adb18-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="adb18-146">Tenga en cuenta que Monitor de red tiene una [*base de datos de propiedades*](p.md) para el analizador que contiene una descripción de todas las propiedades que admite el analizador.</span><span class="sxs-lookup"><span data-stu-id="adb18-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="adb18-147">**Datos de instancia**</span><span class="sxs-lookup"><span data-stu-id="adb18-147">**Instance data**</span></span>

<span data-ttu-id="adb18-148">Los datos de instancia son información que se pasa de un analizador a otro.</span><span class="sxs-lookup"><span data-stu-id="adb18-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="adb18-149">Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere.</span><span class="sxs-lookup"><span data-stu-id="adb18-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="adb18-150">En el parámetro *lpInstData* de las funciones **AttachProperties** y [RecognizeFrame](recognizeframe.md) , monitor de red proporciona un puntero a los datos de instancia del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="adb18-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="adb18-151">Puede establecer los datos de instancia para el analizador durante la implementación de **RecognizeFrame**.</span><span class="sxs-lookup"><span data-stu-id="adb18-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="adb18-152">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="adb18-152">For information on</span></span>                                          | <span data-ttu-id="adb18-153">Vea</span><span class="sxs-lookup"><span data-stu-id="adb18-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="adb18-154">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="adb18-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="adb18-155">Analizadores</span><span class="sxs-lookup"><span data-stu-id="adb18-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="adb18-156">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="adb18-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="adb18-157">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="adb18-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="adb18-158">Cómo reconocer los datos.</span><span class="sxs-lookup"><span data-stu-id="adb18-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="adb18-159">Implementación de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="adb18-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="adb18-160">Cómo crear una base de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="adb18-160">How to create a property database.</span></span>                          | [<span data-ttu-id="adb18-161">Implementación del registro</span><span class="sxs-lookup"><span data-stu-id="adb18-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="adb18-162">Cómo implementar **AttachProperties**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="adb18-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="adb18-163">Implementación de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="adb18-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="adb18-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adb18-164">Requirements</span></span>



| <span data-ttu-id="adb18-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="adb18-165">Requirement</span></span> | <span data-ttu-id="adb18-166">Value</span><span class="sxs-lookup"><span data-stu-id="adb18-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="adb18-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adb18-167">Minimum supported client</span></span><br/> | <span data-ttu-id="adb18-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="adb18-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adb18-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adb18-169">Minimum supported server</span></span><br/> | <span data-ttu-id="adb18-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="adb18-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="adb18-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adb18-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb18-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb18-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb18-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="adb18-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb18-174">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="adb18-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="adb18-175">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="adb18-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="adb18-176">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="adb18-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




