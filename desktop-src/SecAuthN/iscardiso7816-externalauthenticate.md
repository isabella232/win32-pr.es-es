---
description: Construye un comando APDU (unidad de datos de protocolo de aplicación) que actualiza condicionalmente el estado de seguridad, comprobando la identidad del equipo cuando la tarjeta inteligente no confía en él.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816:: ExternalAuthenticate (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423819"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="6a4ac-103">ISCardISO7816:: ExternalAuthenticate (método)</span><span class="sxs-lookup"><span data-stu-id="6a4ac-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="6a4ac-104">\[El método **ExternalAuthenticate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6a4ac-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a4ac-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6a4ac-107">El método **ExternalAuthenticate** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que actualiza condicionalmente el estado de seguridad, comprobando la identidad del equipo cuando la [*tarjeta inteligente*](../secgloss/s-gly.md) no confía en él.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="6a4ac-108">El comando usa el resultado (sí o no) del cálculo de la tarjeta (según un desafío emitido anteriormente por la tarjeta, por ejemplo, mediante el \_ comando ins Get \_ Challenge), una clave (posiblemente secreta) almacenada en la tarjeta y los datos de autenticación transmitidos por el dispositivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4ac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a4ac-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6a4ac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a4ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4ac-111">*byAlgorithmRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4ac-112">Referencia del algoritmo en la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="6a4ac-113">Si este valor es cero, indica que no se proporciona información.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="6a4ac-114">La referencia del algoritmo se conoce antes de emitir el comando o se proporciona en el campo de datos.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ac-115">*bySecretRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4ac-116">Referencia del secreto.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-116">The reference of the secret.</span></span>



| <span data-ttu-id="6a4ac-117">Value</span><span class="sxs-lookup"><span data-stu-id="6a4ac-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="6a4ac-118">Significado</span><span class="sxs-lookup"><span data-stu-id="6a4ac-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="6a4ac-119"><dt>**Sin información**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="6a4ac-120">Posición de bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="6a4ac-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="6a4ac-121">No se proporciona información.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-121">No information is given.</span></span> <span data-ttu-id="6a4ac-122">La referencia del secreto se conoce antes de emitir el comando o se proporciona en el campo de datos.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="6a4ac-123"><dt>**Referencia global**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="6a4ac-124">Posición de bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="6a4ac-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="6a4ac-125">Datos de referencia global (una clave específica de MF).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="6a4ac-126"><dt>**Referencia específica**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="6a4ac-127">Posición de bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="6a4ac-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="6a4ac-128">Datos de referencia específicos (una clave específica de DF).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="6a4ac-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="6a4ac-130">Posición de bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="6a4ac-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="6a4ac-131">00 (otros valores son RFU).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="6a4ac-132"><dt>**Secreto**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="6a4ac-133">Posición de bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="6a4ac-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="6a4ac-134">Número del secreto.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="6a4ac-135">*pChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4ac-136">Puntero a los datos relacionados con la autenticación.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="6a4ac-137">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a4ac-138">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4ac-139">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6a4ac-140">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6a4ac-141">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="6a4ac-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4ac-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a4ac-142">Return value</span></span>

<span data-ttu-id="6a4ac-143">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6a4ac-144">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6a4ac-144">Return code</span></span>                                                                                   | <span data-ttu-id="6a4ac-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a4ac-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6a4ac-146"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6a4ac-147">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="6a4ac-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6a4ac-149">Se pasó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="6a4ac-150"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6a4ac-151">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="6a4ac-152"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6a4ac-153">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6a4ac-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="6a4ac-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a4ac-154">Remarks</span></span>

<span data-ttu-id="6a4ac-155">Para que el comando encapsulado se realice correctamente, el último desafío Obtenido de la tarjeta debe ser válido.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="6a4ac-156">Las comparaciones erróneas se pueden grabar en la tarjeta (por ejemplo, para limitar el número de intentos adicionales de uso de los datos de referencia).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="6a4ac-157">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6a4ac-158">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6a4ac-159">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4ac-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a4ac-160">Requirements</span></span>



| <span data-ttu-id="6a4ac-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4ac-161">Requirement</span></span> | <span data-ttu-id="6a4ac-162">Value</span><span class="sxs-lookup"><span data-stu-id="6a4ac-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4ac-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a4ac-163">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4ac-164">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a4ac-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a4ac-165">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4ac-166">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a4ac-167">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6a4ac-167">End of client support</span></span><br/>    | <span data-ttu-id="6a4ac-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a4ac-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6a4ac-169">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6a4ac-169">End of server support</span></span><br/>    | <span data-ttu-id="6a4ac-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a4ac-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6a4ac-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a4ac-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a4ac-172"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a4ac-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6a4ac-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a4ac-174"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a4ac-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a4ac-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a4ac-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a4ac-177">IID</span><span class="sxs-lookup"><span data-stu-id="6a4ac-177">IID</span></span><br/>                      | <span data-ttu-id="6a4ac-178">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6a4ac-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6a4ac-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a4ac-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4ac-180">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="6a4ac-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
