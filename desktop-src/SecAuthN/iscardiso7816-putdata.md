---
description: El método PutData crea un comando APDU (unidad de datos de protocolo de aplicación) que almacena un solo objeto de datos primitivos o el conjunto de objetos de datos contenidos en un objeto de datos construido, dependiendo del archivo seleccionado.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816::P método utData (Scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911614"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="15919-103">ISCardISO7816::P método utData</span><span class="sxs-lookup"><span data-stu-id="15919-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="15919-104">\[El método **PutData** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="15919-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="15919-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="15919-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15919-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="15919-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="15919-107">El método **PutData** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que almacena un solo objeto de datos primitivos o el conjunto de objetos de datos contenidos en un objeto de datos construido, dependiendo del archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="15919-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="15919-108">El modo en que se almacenan los objetos (al escribir una vez o actualizar o anexar) depende de la definición o de la naturaleza de los objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="15919-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="15919-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15919-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="15919-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15919-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15919-111">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15919-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15919-112">Codificación de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="15919-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="15919-113">Value</span><span class="sxs-lookup"><span data-stu-id="15919-113">Value</span></span>                                                                                  | <span data-ttu-id="15919-114">Significado</span><span class="sxs-lookup"><span data-stu-id="15919-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="15919-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="15919-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="15919-116">RFU</span><span class="sxs-lookup"><span data-stu-id="15919-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="15919-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="15919-118">Etiqueta BER-TLV (1 byte) en P2</span><span class="sxs-lookup"><span data-stu-id="15919-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="15919-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="15919-120">Datos de aplicación (codificación propietaria)</span><span class="sxs-lookup"><span data-stu-id="15919-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="15919-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="15919-122">Etiqueta SIMPLE-TLV en P2</span><span class="sxs-lookup"><span data-stu-id="15919-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="15919-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="15919-124">RFU</span><span class="sxs-lookup"><span data-stu-id="15919-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="15919-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="15919-126">Etiqueta BER-TLV (2 bytes) en P1-P2</span><span class="sxs-lookup"><span data-stu-id="15919-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="15919-127">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15919-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15919-128">Codificación de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="15919-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="15919-129">Value</span><span class="sxs-lookup"><span data-stu-id="15919-129">Value</span></span>                                                                                  | <span data-ttu-id="15919-130">Significado</span><span class="sxs-lookup"><span data-stu-id="15919-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="15919-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="15919-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="15919-132">RFU</span><span class="sxs-lookup"><span data-stu-id="15919-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="15919-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="15919-134">Etiqueta BER-TLV (1 byte) en P2</span><span class="sxs-lookup"><span data-stu-id="15919-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="15919-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="15919-136">Datos de aplicación (codificación propietaria)</span><span class="sxs-lookup"><span data-stu-id="15919-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="15919-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="15919-138">Etiqueta SIMPLE-TLV en P2</span><span class="sxs-lookup"><span data-stu-id="15919-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="15919-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="15919-140">RFU</span><span class="sxs-lookup"><span data-stu-id="15919-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="15919-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="15919-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="15919-142">Etiqueta BER-TLV (2 bytes) en P1-P2</span><span class="sxs-lookup"><span data-stu-id="15919-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="15919-143">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15919-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15919-144">Puntero a un búfer de bytes que contiene los parámetros y los datos que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="15919-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="15919-145">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="15919-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15919-146">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="15919-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="15919-147">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="15919-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="15919-148">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="15919-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15919-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15919-149">Return value</span></span>

<span data-ttu-id="15919-150">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="15919-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="15919-151">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="15919-151">Return code</span></span>                                                                                   | <span data-ttu-id="15919-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="15919-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="15919-153"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="15919-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="15919-154">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="15919-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="15919-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="15919-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="15919-156">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="15919-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="15919-157"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="15919-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="15919-158">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="15919-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="15919-159"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="15919-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="15919-160">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="15919-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="15919-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15919-161">Remarks</span></span>

<span data-ttu-id="15919-162">El comando solo se puede realizar si el estado de seguridad satisface las condiciones de seguridad definidas por la aplicación en el [*contexto*](../secgloss/c-gly.md) de la función.</span><span class="sxs-lookup"><span data-stu-id="15919-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="15919-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Almacenar datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="15919-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="15919-164">Cuando el valor de P1-P2 se encuentra en el intervalo de 0100 a 01FF, el valor de P1-P2 será un identificador reservado para las pruebas internas de tarjeta y para los servicios de propiedad significativos en un contexto de aplicación determinado.</span><span class="sxs-lookup"><span data-stu-id="15919-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="15919-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Almacenar objetos de datos</span><span class="sxs-lookup"><span data-stu-id="15919-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="15919-166">Cuando el valor P1-P2 se encuentra en el intervalo de 0040 a 00FF, el valor de P2 será una etiqueta BER-TLV en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="15919-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="15919-167">El valor de 00FF se reserva para indicar que el campo de datos incluye objetos de datos BER-TLV.</span><span class="sxs-lookup"><span data-stu-id="15919-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="15919-168">Cuando el valor de P1-P2 se encuentra en el intervalo de 0200 a 02FF, el valor de P2 será una etiqueta SIMPLE-TLV.</span><span class="sxs-lookup"><span data-stu-id="15919-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="15919-169">El valor 0200 es RFU.</span><span class="sxs-lookup"><span data-stu-id="15919-169">The value 0200 is RFU.</span></span> <span data-ttu-id="15919-170">El valor 02FF se reserva para indicar que el campo de datos incluye objetos de datos simples-TLV.</span><span class="sxs-lookup"><span data-stu-id="15919-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="15919-171">Cuando el valor de P1-P2 se encuentra en el intervalo de 4000 a FFFF, el valor de P1-P2 será una etiqueta BER-TLV en dos bytes.</span><span class="sxs-lookup"><span data-stu-id="15919-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="15919-172">Los valores 4000 a FFFF son RFU.</span><span class="sxs-lookup"><span data-stu-id="15919-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="15919-173">Cuando se proporciona un objeto de datos primitivo, el campo de datos del mensaje de comando contendrá el valor del objeto de datos primitivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="15919-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="15919-174">Cuando se proporciona un objeto de datos construido, el campo de datos del mensaje de comando contendrá el valor del objeto de datos construido (es decir, los objetos de datos, incluida su etiqueta, longitud y valor).</span><span class="sxs-lookup"><span data-stu-id="15919-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="15919-175">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="15919-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="15919-176">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15919-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="15919-177">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="15919-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15919-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15919-178">Requirements</span></span>



| <span data-ttu-id="15919-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="15919-179">Requirement</span></span> | <span data-ttu-id="15919-180">Value</span><span class="sxs-lookup"><span data-stu-id="15919-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15919-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15919-181">Minimum supported client</span></span><br/> | <span data-ttu-id="15919-182">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="15919-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="15919-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15919-183">Minimum supported server</span></span><br/> | <span data-ttu-id="15919-184">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15919-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15919-185">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="15919-185">End of client support</span></span><br/>    | <span data-ttu-id="15919-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="15919-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="15919-187">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="15919-187">End of server support</span></span><br/>    | <span data-ttu-id="15919-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15919-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="15919-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15919-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="15919-190"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="15919-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15919-191">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="15919-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="15919-192"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15919-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15919-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15919-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15919-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15919-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15919-195">IID</span><span class="sxs-lookup"><span data-stu-id="15919-195">IID</span></span><br/>                      | <span data-ttu-id="15919-196">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="15919-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="15919-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="15919-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15919-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="15919-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="15919-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="15919-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
