---
description: El método UpdateRecord crea un comando de unidad de datos de protocolo de aplicación (APDU) que actualiza un registro específico con los bits especificados en el comando APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'ISCardISO7816:: UpdateRecord (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277018"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="d48f9-103">ISCardISO7816:: UpdateRecord (método)</span><span class="sxs-lookup"><span data-stu-id="d48f9-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="d48f9-104">\[El método **UpdateRecord** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d48f9-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d48f9-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d48f9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d48f9-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d48f9-107">El método **UpdateRecord** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que actualiza un registro específico con los bits especificados en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="d48f9-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="d48f9-108">Al usar el direccionamiento de registros actual, el comando establece el puntero de registro en el registro actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d48f9-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d48f9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d48f9-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="d48f9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d48f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48f9-111">*byRecordId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48f9-112">Valor P1:</span><span class="sxs-lookup"><span data-stu-id="d48f9-112">P1 value:</span></span>

<span data-ttu-id="d48f9-113">P1 = 00 designa el registro actual</span><span class="sxs-lookup"><span data-stu-id="d48f9-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="d48f9-114">P1! = ' 00 ' es el número del registro especificado</span><span class="sxs-lookup"><span data-stu-id="d48f9-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="d48f9-115">*byRefCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48f9-116">Codificación del control de referencia P2:</span><span class="sxs-lookup"><span data-stu-id="d48f9-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="d48f9-117">Value</span><span class="sxs-lookup"><span data-stu-id="d48f9-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="d48f9-118">Significado</span><span class="sxs-lookup"><span data-stu-id="d48f9-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="d48f9-119"><dt>**EF actual**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="d48f9-120">Posición de bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="d48f9-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="d48f9-121">EF actualmente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d48f9-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="d48f9-122"><dt>**Short EF ID**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="d48f9-123">Posición de bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="d48f9-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="d48f9-124">Identificador de EF corto.</span><span class="sxs-lookup"><span data-stu-id="d48f9-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="d48f9-125"><dt>**Primer registro**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="d48f9-126">Posición de bit:-----000</span><span class="sxs-lookup"><span data-stu-id="d48f9-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="d48f9-127"><dt>**Último registro**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="d48f9-128">Posición de bit:-----001</span><span class="sxs-lookup"><span data-stu-id="d48f9-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="d48f9-129"><dt>**Siguiente registro**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="d48f9-130">Posición de bit:-----010</span><span class="sxs-lookup"><span data-stu-id="d48f9-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="d48f9-131"><dt>**Registro anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="d48f9-132">Posición de bit:-----011</span><span class="sxs-lookup"><span data-stu-id="d48f9-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="d48f9-133"><dt>**Registro \# en P1**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="d48f9-134">Posición de bit:-----100</span><span class="sxs-lookup"><span data-stu-id="d48f9-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="d48f9-135">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48f9-136">Puntero al registro que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="d48f9-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="d48f9-137">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d48f9-138">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="d48f9-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="d48f9-139">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="d48f9-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="d48f9-140">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="d48f9-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48f9-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d48f9-141">Return value</span></span>

<span data-ttu-id="d48f9-142">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d48f9-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d48f9-143">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d48f9-143">Return code</span></span>                                                                                   | <span data-ttu-id="d48f9-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="d48f9-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d48f9-145"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d48f9-146">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d48f9-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d48f9-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d48f9-148">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d48f9-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d48f9-149"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d48f9-150">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="d48f9-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d48f9-151"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d48f9-152">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d48f9-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d48f9-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d48f9-153">Remarks</span></span>

<span data-ttu-id="d48f9-154">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="d48f9-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="d48f9-155">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="d48f9-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="d48f9-156">Si hay otro archivo elemental seleccionado actualmente en el momento de emitir este comando, este comando se puede procesar sin identificación del archivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="d48f9-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="d48f9-157">Si el comando construido se aplica a un archivo elemental fijo lineal o con estructura cíclica, se anulará si la longitud del registro es diferente de la longitud del registro existente.</span><span class="sxs-lookup"><span data-stu-id="d48f9-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="d48f9-158">Si el comando se aplica a un archivo elemental estructurado de variable lineal, se puede realizar cuando la longitud del registro es diferente de la longitud del registro existente.</span><span class="sxs-lookup"><span data-stu-id="d48f9-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="d48f9-159">La opción "anterior" del comando (P2 = xxxxx011), que se aplica a un archivo cíclico, tiene el mismo comportamiento que un comando construido por [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="d48f9-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="d48f9-160">No se pueden leer los archivos elementales sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="d48f9-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="d48f9-161">El comando construido se anula si se aplica a un archivo elemental sin la estructura del registro.</span><span class="sxs-lookup"><span data-stu-id="d48f9-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="d48f9-162">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="d48f9-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="d48f9-163">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d48f9-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d48f9-164">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d48f9-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d48f9-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d48f9-165">Requirements</span></span>



| <span data-ttu-id="d48f9-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="d48f9-166">Requirement</span></span> | <span data-ttu-id="d48f9-167">Value</span><span class="sxs-lookup"><span data-stu-id="d48f9-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48f9-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d48f9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d48f9-169">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d48f9-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d48f9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d48f9-171">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d48f9-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d48f9-172">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d48f9-172">End of client support</span></span><br/>    | <span data-ttu-id="d48f9-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d48f9-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d48f9-174">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d48f9-174">End of server support</span></span><br/>    | <span data-ttu-id="d48f9-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d48f9-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d48f9-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d48f9-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="d48f9-177"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d48f9-178">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d48f9-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="d48f9-179"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d48f9-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d48f9-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48f9-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48f9-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d48f9-182">IID</span><span class="sxs-lookup"><span data-stu-id="d48f9-182">IID</span></span><br/>                      | <span data-ttu-id="d48f9-183">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d48f9-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="d48f9-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="d48f9-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48f9-185">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="d48f9-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="d48f9-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="d48f9-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="d48f9-187">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="d48f9-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="d48f9-188">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="d48f9-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
