---
description: Crea un comando APDU (unidad de datos de protocolo de aplicación) que inicia la comparación (en la tarjeta) de los datos de comprobación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, contraseña).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816:: verify (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652765"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="565d2-103">ISCardISO7816:: verify (método)</span><span class="sxs-lookup"><span data-stu-id="565d2-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="565d2-104">\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="565d2-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="565d2-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="565d2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="565d2-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="565d2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="565d2-107">El método **Verify** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que inicia la comparación (en la tarjeta) de los datos de comprobación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, password).</span><span class="sxs-lookup"><span data-stu-id="565d2-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="565d2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="565d2-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="565d2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="565d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="565d2-110">*byRefCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="565d2-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="565d2-111">Un cuantificador de los datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="565d2-111">A quantifier of the reference data.</span></span> <span data-ttu-id="565d2-112">A continuación se muestra la codificación del control de referencia P2.</span><span class="sxs-lookup"><span data-stu-id="565d2-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="565d2-113">Cuando el cuerpo está vacío, el comando se puede usar para recuperar el número ' X ' de reintentos más permitidos (SW1-SW2 = 63CX) o para comprobar si la comprobación no es necesaria (SW1-SW2 = 9000).</span><span class="sxs-lookup"><span data-stu-id="565d2-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="565d2-114">Value</span><span class="sxs-lookup"><span data-stu-id="565d2-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="565d2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="565d2-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="565d2-116"><dt>**Sin información**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="565d2-117">Posición de bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="565d2-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="565d2-118">P2 = 00 está reservado para indicar que no se usa ningún calificador determinado en esas tarjetas donde el comando Verify hace referencia a los datos secretos de forma inequívoca.</span><span class="sxs-lookup"><span data-stu-id="565d2-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="565d2-119"><dt>**Referencia global**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="565d2-120">Posición de bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="565d2-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="565d2-121">Un ejemplo de referencia global sería una contraseña.</span><span class="sxs-lookup"><span data-stu-id="565d2-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="565d2-122"><dt>**Referencia específica**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="565d2-123">Posición de bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="565d2-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="565d2-124">Un ejemplo de referencia específica es la contraseña específica de DF.</span><span class="sxs-lookup"><span data-stu-id="565d2-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="565d2-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="565d2-126">Posición de bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="565d2-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="565d2-127"><dt>**Datos de referencia \#**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="565d2-128">Posición de bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="565d2-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="565d2-129">El número de datos de referencia puede ser, por ejemplo, un número de contraseña o un identificador de EF corto.</span><span class="sxs-lookup"><span data-stu-id="565d2-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="565d2-130">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="565d2-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="565d2-131">Puntero a los datos de comprobación.</span><span class="sxs-lookup"><span data-stu-id="565d2-131">A pointer to the verification data.</span></span> <span data-ttu-id="565d2-132">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="565d2-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="565d2-133">El valor predeterminado es **NULL**.</span><span class="sxs-lookup"><span data-stu-id="565d2-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="565d2-134">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="565d2-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="565d2-135">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="565d2-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="565d2-136">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="565d2-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="565d2-137">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="565d2-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="565d2-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="565d2-138">Return value</span></span>

<span data-ttu-id="565d2-139">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="565d2-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="565d2-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="565d2-140">Return code</span></span>                                                                                   | <span data-ttu-id="565d2-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="565d2-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="565d2-142"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="565d2-143">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="565d2-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="565d2-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="565d2-145">Se usó un parámetro que no es válido.</span><span class="sxs-lookup"><span data-stu-id="565d2-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="565d2-146"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="565d2-147">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="565d2-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="565d2-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="565d2-149">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="565d2-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="565d2-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="565d2-150">Remarks</span></span>

<span data-ttu-id="565d2-151">El estado de seguridad puede modificarse como resultado de una comparación.</span><span class="sxs-lookup"><span data-stu-id="565d2-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="565d2-152">Las comparaciones erróneas se pueden grabar en la tarjeta (por ejemplo, para limitar el número de intentos adicionales de uso de los datos de referencia).</span><span class="sxs-lookup"><span data-stu-id="565d2-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="565d2-153">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="565d2-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="565d2-154">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="565d2-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="565d2-155">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="565d2-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="565d2-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="565d2-156">Requirements</span></span>



| <span data-ttu-id="565d2-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="565d2-157">Requirement</span></span> | <span data-ttu-id="565d2-158">Value</span><span class="sxs-lookup"><span data-stu-id="565d2-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="565d2-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="565d2-159">Minimum supported client</span></span><br/> | <span data-ttu-id="565d2-160">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="565d2-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="565d2-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="565d2-161">Minimum supported server</span></span><br/> | <span data-ttu-id="565d2-162">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="565d2-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="565d2-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="565d2-163">End of client support</span></span><br/>    | <span data-ttu-id="565d2-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="565d2-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="565d2-165">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="565d2-165">End of server support</span></span><br/>    | <span data-ttu-id="565d2-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="565d2-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="565d2-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="565d2-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="565d2-168"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="565d2-169">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="565d2-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="565d2-170"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="565d2-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="565d2-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="565d2-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="565d2-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="565d2-173">IID</span><span class="sxs-lookup"><span data-stu-id="565d2-173">IID</span></span><br/>                      | <span data-ttu-id="565d2-174">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="565d2-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="565d2-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="565d2-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565d2-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="565d2-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
