---
description: Construye un comando APDU (unidad de datos de protocolo de aplicación) que inicia el cálculo de los datos de autenticación por la tarjeta utilizando los datos de desafío enviados desde el dispositivo de interfaz y un secreto pertinente (por ejemplo, una clave) almacenado en la tarjeta.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816:: InternalAuthenticate (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082457"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="481f4-103">ISCardISO7816:: InternalAuthenticate (método)</span><span class="sxs-lookup"><span data-stu-id="481f4-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="481f4-104">\[El método **InternalAuthenticate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="481f4-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="481f4-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="481f4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="481f4-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="481f4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="481f4-107">El método **InternalAuthenticate** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que inicia el cálculo de los datos de autenticación por la tarjeta utilizando los datos de desafío enviados desde el dispositivo de interfaz y un secreto pertinente (por ejemplo, una clave) almacenados en la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="481f4-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="481f4-108">Cuando el secreto pertinente se adjunta al MF, el comando puede usarse para autenticar la tarjeta en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="481f4-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="481f4-109">Cuando el secreto pertinente se adjunta a otro DF, el comando se puede usar para autenticar el DF.</span><span class="sxs-lookup"><span data-stu-id="481f4-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="481f4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="481f4-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="481f4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="481f4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="481f4-112">*byAlgorithmRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481f4-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481f4-113">Referencia del algoritmo en la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="481f4-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="481f4-114">Si este valor es cero, indica que no se proporciona información.</span><span class="sxs-lookup"><span data-stu-id="481f4-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="481f4-115">La referencia del algoritmo se conoce antes de emitir el comando o se proporciona en el campo de datos.</span><span class="sxs-lookup"><span data-stu-id="481f4-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="481f4-116">*bySecretRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481f4-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481f4-117">Referencia del secreto.</span><span class="sxs-lookup"><span data-stu-id="481f4-117">Reference of the secret.</span></span>



| <span data-ttu-id="481f4-118">Value</span><span class="sxs-lookup"><span data-stu-id="481f4-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="481f4-119">Significado</span><span class="sxs-lookup"><span data-stu-id="481f4-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="481f4-120"><dt>**Sin información**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="481f4-121">Posición de bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="481f4-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="481f4-122">No se proporciona información.</span><span class="sxs-lookup"><span data-stu-id="481f4-122">No information is given.</span></span> <span data-ttu-id="481f4-123">La referencia del secreto se conoce antes de emitir el comando o se proporciona en el campo de datos.</span><span class="sxs-lookup"><span data-stu-id="481f4-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="481f4-124"><dt>**Referencia global**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="481f4-125">Posición de bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="481f4-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="481f4-126">Datos de referencia global (una clave específica de MF).</span><span class="sxs-lookup"><span data-stu-id="481f4-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="481f4-127"><dt>**Referencia específica**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="481f4-128">Posición de bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="481f4-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="481f4-129">Datos de referencia específicos (una clave específica de DF).</span><span class="sxs-lookup"><span data-stu-id="481f4-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="481f4-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="481f4-131">Posición de bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="481f4-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="481f4-132">00 (otros valores son RFU).</span><span class="sxs-lookup"><span data-stu-id="481f4-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="481f4-133"><dt>**Secreto**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="481f4-134">Posición de bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="481f4-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="481f4-135">Número del secreto.</span><span class="sxs-lookup"><span data-stu-id="481f4-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="481f4-136">*pChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481f4-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481f4-137">Puntero a los datos relacionados con la autenticación (por ejemplo, Challenge).</span><span class="sxs-lookup"><span data-stu-id="481f4-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="481f4-138">*lReplyBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="481f4-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481f4-139">Número máximo de bytes esperados en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="481f4-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="481f4-140">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="481f4-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="481f4-141">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="481f4-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="481f4-142">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="481f4-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="481f4-143">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="481f4-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="481f4-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="481f4-144">Return value</span></span>

<span data-ttu-id="481f4-145">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="481f4-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="481f4-146">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="481f4-146">Return code</span></span>                                                                                   | <span data-ttu-id="481f4-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="481f4-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="481f4-148"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="481f4-149">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="481f4-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="481f4-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="481f4-151">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="481f4-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="481f4-152"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="481f4-153">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="481f4-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="481f4-154"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="481f4-155">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="481f4-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="481f4-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="481f4-156">Remarks</span></span>

<span data-ttu-id="481f4-157">La ejecución correcta del comando puede estar sujeta a la finalización correcta de los comandos anteriores (por ejemplo, comprobar o seleccionar archivo) o selecciones (por ejemplo, el secreto relevante).</span><span class="sxs-lookup"><span data-stu-id="481f4-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="481f4-158">Si una clave y un algoritmo están seleccionados actualmente al emitir el comando, el comando puede usar implícitamente la clave y el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="481f4-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="481f4-159">El número de veces que se emite el comando se puede registrar en la tarjeta para limitar el número de intentos posteriores de usar el secreto o el algoritmo pertinente.</span><span class="sxs-lookup"><span data-stu-id="481f4-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="481f4-160">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="481f4-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="481f4-161">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="481f4-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="481f4-162">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="481f4-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="481f4-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="481f4-163">Requirements</span></span>



| <span data-ttu-id="481f4-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="481f4-164">Requirement</span></span> | <span data-ttu-id="481f4-165">Value</span><span class="sxs-lookup"><span data-stu-id="481f4-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="481f4-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="481f4-166">Minimum supported client</span></span><br/> | <span data-ttu-id="481f4-167">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="481f4-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="481f4-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="481f4-168">Minimum supported server</span></span><br/> | <span data-ttu-id="481f4-169">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="481f4-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="481f4-170">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="481f4-170">End of client support</span></span><br/>    | <span data-ttu-id="481f4-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="481f4-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="481f4-172">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="481f4-172">End of server support</span></span><br/>    | <span data-ttu-id="481f4-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="481f4-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="481f4-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="481f4-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="481f4-175"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="481f4-176">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="481f4-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="481f4-177"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="481f4-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="481f4-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="481f4-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="481f4-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="481f4-180">IID</span><span class="sxs-lookup"><span data-stu-id="481f4-180">IID</span></span><br/>                      | <span data-ttu-id="481f4-181">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="481f4-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="481f4-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="481f4-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="481f4-183">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="481f4-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="481f4-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="481f4-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
