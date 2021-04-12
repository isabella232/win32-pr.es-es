---
description: Construye un comando APDU que inicia una de las operaciones de la lista.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816:: WriteRecord (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153833"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="2b0ea-103">ISCardISO7816:: WriteRecord (método)</span><span class="sxs-lookup"><span data-stu-id="2b0ea-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="2b0ea-104">\[El método **WriteRecord** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b0ea-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b0ea-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2b0ea-107">El método **WriteRecord** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que inicia una de las operaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b0ea-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="2b0ea-108">La escritura una vez de un registro.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-108">The write once of a record.</span></span>
-   <span data-ttu-id="2b0ea-109">El operador lógico **or** de los bytes de datos de un registro que ya está presente en la tarjeta con los bytes de datos del registro dado en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="2b0ea-110">El AND lógico de los bytes de datos de un registro ya está presente en la tarjeta con los bytes de datos del registro dado en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="2b0ea-111">Cuando no se especifica ninguna indicación en el byte de codificación de datos, se aplica el comportamiento lógico OR.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="2b0ea-112">Al usar el direccionamiento de registros actual, el comando establece el puntero de registro en el registro actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b0ea-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b0ea-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="2b0ea-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b0ea-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b0ea-115">*byRecordId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0ea-116">Identificación del registro.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-116">Record identification.</span></span> <span data-ttu-id="2b0ea-117">Este es el valor P1:</span><span class="sxs-lookup"><span data-stu-id="2b0ea-117">This is the P1 value:</span></span>

<span data-ttu-id="2b0ea-118">P1 = ' 00 ' designa el registro actual.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="2b0ea-119">P1! = ' 00 ' es el número del registro especificado.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="2b0ea-120">*byRefCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0ea-121">Codificación del control de referencia P2.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="2b0ea-122">Value</span><span class="sxs-lookup"><span data-stu-id="2b0ea-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="2b0ea-123">Significado</span><span class="sxs-lookup"><span data-stu-id="2b0ea-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="2b0ea-124"><dt>**EF actual**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="2b0ea-125">Posición de bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="2b0ea-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="2b0ea-126">EF actualmente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="2b0ea-127"><dt>**Short EF ID**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="2b0ea-128">Posición de bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="2b0ea-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="2b0ea-129">Identificador de EF corto.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="2b0ea-130"><dt>**Primer registro**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="2b0ea-131">Posición de bit:-----000</span><span class="sxs-lookup"><span data-stu-id="2b0ea-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="2b0ea-132"><dt>**Último registro**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="2b0ea-133">Posición de bit:-----001</span><span class="sxs-lookup"><span data-stu-id="2b0ea-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="2b0ea-134"><dt>**Siguiente registro**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="2b0ea-135">Posición de bit:-----010</span><span class="sxs-lookup"><span data-stu-id="2b0ea-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="2b0ea-136"><dt>**Registro anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="2b0ea-137">Posición de bit:-----011</span><span class="sxs-lookup"><span data-stu-id="2b0ea-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="2b0ea-138"><dt>**Registro \# en P1**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="2b0ea-139">Posición de bit:-----100</span><span class="sxs-lookup"><span data-stu-id="2b0ea-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="2b0ea-140">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0ea-141">Puntero al registro que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="2b0ea-142">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0ea-143">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="2b0ea-144">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="2b0ea-145">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="2b0ea-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b0ea-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b0ea-146">Return value</span></span>

<span data-ttu-id="2b0ea-147">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2b0ea-148">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2b0ea-148">Return code</span></span>                                                                                   | <span data-ttu-id="2b0ea-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b0ea-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2b0ea-150"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2b0ea-151">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2b0ea-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2b0ea-153">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2b0ea-154"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2b0ea-155">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="2b0ea-156"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2b0ea-157">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="2b0ea-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2b0ea-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b0ea-158">Remarks</span></span>

<span data-ttu-id="2b0ea-159">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="2b0ea-160">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="2b0ea-161">Si hay otro archivo elemental seleccionado actualmente en el momento de emitir este comando, este comando se puede procesar sin identificación del archivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="2b0ea-162">Si el comando encapsulado se aplica a un archivo elemental fijo o con estructura lineal, se anulará si la longitud del registro es diferente de la longitud del registro existente.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="2b0ea-163">Si se aplica a un archivo elemental estructurado de variable lineal, se puede realizar cuando la longitud del registro es diferente de la longitud del registro existente.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="2b0ea-164">Si P2 = xxxxx011 y el archivo elemental es un archivo cíclico, este comando tiene el mismo comportamiento que un comando construido con [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ea-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="2b0ea-165">No se puede escribir en los archivos elementales sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="2b0ea-166">El comando construido se anula si se aplica a un archivo elemental sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="2b0ea-167">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ea-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="2b0ea-168">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b0ea-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2b0ea-169">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ea-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0ea-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b0ea-170">Requirements</span></span>



| <span data-ttu-id="2b0ea-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b0ea-171">Requirement</span></span> | <span data-ttu-id="2b0ea-172">Value</span><span class="sxs-lookup"><span data-stu-id="2b0ea-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0ea-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b0ea-173">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0ea-174">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2b0ea-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b0ea-175">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0ea-176">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b0ea-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b0ea-177">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2b0ea-177">End of client support</span></span><br/>    | <span data-ttu-id="2b0ea-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b0ea-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2b0ea-179">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2b0ea-179">End of server support</span></span><br/>    | <span data-ttu-id="2b0ea-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b0ea-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2b0ea-181">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b0ea-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b0ea-182"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b0ea-183">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b0ea-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b0ea-184"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b0ea-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b0ea-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0ea-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ea-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b0ea-187">IID</span><span class="sxs-lookup"><span data-stu-id="2b0ea-187">IID</span></span><br/>                      | <span data-ttu-id="2b0ea-188">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2b0ea-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2b0ea-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b0ea-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0ea-190">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="2b0ea-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="2b0ea-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="2b0ea-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="2b0ea-192">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="2b0ea-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="2b0ea-193">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="2b0ea-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
