---
description: El método ReadRecord crea un comando de unidad de datos de protocolo de aplicación (APDU) que lee el contenido de los registros especificados o la parte inicial de un registro de un archivo elemental.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816:: ReadRecord (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082614"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="8549d-103">ISCardISO7816:: ReadRecord (método)</span><span class="sxs-lookup"><span data-stu-id="8549d-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="8549d-104">\[El método **ReadRecord** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8549d-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8549d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8549d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8549d-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8549d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8549d-107">El método **ReadRecord** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que lee el contenido de los registros especificados o la parte inicial de un registro de un archivo elemental.</span><span class="sxs-lookup"><span data-stu-id="8549d-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8549d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8549d-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8549d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8549d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8549d-110">*byRecordId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8549d-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8549d-111">Número de registro o identificador del primer registro que se va a leer (00 indica el registro actual).</span><span class="sxs-lookup"><span data-stu-id="8549d-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="8549d-112">*byRefCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8549d-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8549d-113">Codificación del control de referencia.</span><span class="sxs-lookup"><span data-stu-id="8549d-113">Coding of the reference control.</span></span>



| <span data-ttu-id="8549d-114">Value</span><span class="sxs-lookup"><span data-stu-id="8549d-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="8549d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8549d-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="8549d-116"><dt>**EF actual**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="8549d-117">Posición de bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="8549d-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="8549d-118">EF actualmente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8549d-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="8549d-119"><dt>**Short EF ID**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="8549d-120">Posición de bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="8549d-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="8549d-121">Identificador de EF corto.</span><span class="sxs-lookup"><span data-stu-id="8549d-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="8549d-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="8549d-123">Posición de bit: 11111---</span><span class="sxs-lookup"><span data-stu-id="8549d-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="8549d-124"><dt>**Record \#**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="8549d-125">Posición de bit:-----1xx</span><span class="sxs-lookup"><span data-stu-id="8549d-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="8549d-126">Uso del número de registro en P1.</span><span class="sxs-lookup"><span data-stu-id="8549d-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="8549d-127"><dt>**Leer registro**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="8549d-128">Posición de bit:-----100</span><span class="sxs-lookup"><span data-stu-id="8549d-128">Bit position: -----100</span></span><br/> <span data-ttu-id="8549d-129">Lea el registro P1.</span><span class="sxs-lookup"><span data-stu-id="8549d-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="8549d-130"><dt>**Hasta el último**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="8549d-131">Posición de bit:-----101</span><span class="sxs-lookup"><span data-stu-id="8549d-131">Bit position: -----101</span></span><br/> <span data-ttu-id="8549d-132">Lea todos los registros de P1 hasta el último.</span><span class="sxs-lookup"><span data-stu-id="8549d-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="8549d-133"><dt>**Hasta P1**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="8549d-134">Posición de bit:-----110</span><span class="sxs-lookup"><span data-stu-id="8549d-134">Bit position: -----110</span></span><br/> <span data-ttu-id="8549d-135">Lea todos los registros del último hasta el P1.</span><span class="sxs-lookup"><span data-stu-id="8549d-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="8549d-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="8549d-137">Posición de bit:-----111</span><span class="sxs-lookup"><span data-stu-id="8549d-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="8549d-138"><dt>**Record ID**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="8549d-139">Posición de bit:-----0xx</span><span class="sxs-lookup"><span data-stu-id="8549d-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="8549d-140">Uso del número de registro en P1.</span><span class="sxs-lookup"><span data-stu-id="8549d-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="8549d-141"><dt>**Primera vez**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="8549d-142">Posición de bit:-----000</span><span class="sxs-lookup"><span data-stu-id="8549d-142">Bit position: -----000</span></span><br/> <span data-ttu-id="8549d-143">Lea la primera aparición.</span><span class="sxs-lookup"><span data-stu-id="8549d-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="8549d-144"><dt>**Última vez**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="8549d-145">Posición de bit:-----001</span><span class="sxs-lookup"><span data-stu-id="8549d-145">Bit position: -----001</span></span><br/> <span data-ttu-id="8549d-146">Leer la última aparición.</span><span class="sxs-lookup"><span data-stu-id="8549d-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="8549d-147"><dt>**Siguiente sucede**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="8549d-148">Posición de bit:-----010</span><span class="sxs-lookup"><span data-stu-id="8549d-148">Bit position: -----010</span></span><br/> <span data-ttu-id="8549d-149">Lea la siguiente repetición.</span><span class="sxs-lookup"><span data-stu-id="8549d-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="8549d-150"><dt>**Anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="8549d-151">Posición de bit:-----011</span><span class="sxs-lookup"><span data-stu-id="8549d-151">Bit position: -----011</span></span><br/> <span data-ttu-id="8549d-152">Lee la repetición anterior.</span><span class="sxs-lookup"><span data-stu-id="8549d-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="8549d-153"><dt>**Secreto**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="8549d-154">Posición de bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="8549d-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="8549d-155">*lBytesToRead* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8549d-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8549d-156">Número de bytes que se van a leer del EF transparente.</span><span class="sxs-lookup"><span data-stu-id="8549d-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="8549d-157">Si el campo le contiene solo ceros, dependiendo de b3b2b1 de P2 y dentro del límite de 256 para la longitud corta o 65536 para la longitud extendida, el comando debe leer por completo el registro solicitado único o la secuencia de registros solicitada.</span><span class="sxs-lookup"><span data-stu-id="8549d-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="8549d-158">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8549d-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8549d-159">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="8549d-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="8549d-160">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="8549d-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="8549d-161">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="8549d-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8549d-162">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8549d-162">Return value</span></span>

<span data-ttu-id="8549d-163">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="8549d-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8549d-164">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8549d-164">Return code</span></span>                                                                                   | <span data-ttu-id="8549d-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="8549d-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8549d-166"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8549d-167">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="8549d-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8549d-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8549d-169">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8549d-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8549d-170"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8549d-171">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="8549d-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8549d-172"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8549d-173">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="8549d-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8549d-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8549d-174">Remarks</span></span>

<span data-ttu-id="8549d-175">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está leyendo.</span><span class="sxs-lookup"><span data-stu-id="8549d-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="8549d-176">Si hay otro archivo elemental seleccionado actualmente en el momento de emitir este comando, se puede procesar sin identificación del archivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="8549d-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="8549d-177">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="8549d-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="8549d-178">No se pueden leer los archivos elementales sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="8549d-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="8549d-179">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="8549d-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="8549d-180">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="8549d-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="8549d-181">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8549d-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8549d-182">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8549d-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8549d-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8549d-183">Requirements</span></span>



| <span data-ttu-id="8549d-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="8549d-184">Requirement</span></span> | <span data-ttu-id="8549d-185">Value</span><span class="sxs-lookup"><span data-stu-id="8549d-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8549d-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8549d-186">Minimum supported client</span></span><br/> | <span data-ttu-id="8549d-187">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8549d-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8549d-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8549d-188">Minimum supported server</span></span><br/> | <span data-ttu-id="8549d-189">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8549d-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8549d-190">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8549d-190">End of client support</span></span><br/>    | <span data-ttu-id="8549d-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8549d-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8549d-192">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8549d-192">End of server support</span></span><br/>    | <span data-ttu-id="8549d-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8549d-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8549d-194">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8549d-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="8549d-195"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8549d-196">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8549d-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="8549d-197"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8549d-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8549d-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8549d-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8549d-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8549d-200">IID</span><span class="sxs-lookup"><span data-stu-id="8549d-200">IID</span></span><br/>                      | <span data-ttu-id="8549d-201">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8549d-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8549d-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="8549d-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8549d-203">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="8549d-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="8549d-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8549d-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="8549d-205">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="8549d-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="8549d-206">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="8549d-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
