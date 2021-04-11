---
description: El método AppendRecord crea un comando APDU (unidad de datos de protocolo de aplicación) que anexa un registro al final de un archivo elemental estructurado linealmente (EF) o escribe el registro número 1 en un archivo elemental estructurado de forma cíclica.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'ISCardISO7816:: AppendRecord (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275914"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="6f3db-103">ISCardISO7816:: AppendRecord (método)</span><span class="sxs-lookup"><span data-stu-id="6f3db-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="6f3db-104">\[El método **AppendRecord** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6f3db-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f3db-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6f3db-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f3db-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6f3db-107">El método **AppendRecord** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que anexa un registro al final de un archivo elemental estructurado linealmente (EF) o escribe el registro número 1 en un archivo elemental estructurado de forma cíclica.</span><span class="sxs-lookup"><span data-stu-id="6f3db-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f3db-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6f3db-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f3db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f3db-110">*byRefCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3db-111">Identifica el archivo elemental que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="6f3db-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="6f3db-112">Value</span><span class="sxs-lookup"><span data-stu-id="6f3db-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="6f3db-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6f3db-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="6f3db-114"><dt>**EF actual**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="6f3db-115">Posición de bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="6f3db-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="6f3db-116"><dt>**Short EF ID**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="6f3db-117">Posición de bits: XXXXX000</span><span class="sxs-lookup"><span data-stu-id="6f3db-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="6f3db-118"><dt>**Reservado**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="6f3db-119">Posición de bit: xxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="6f3db-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f3db-120">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3db-121">Puntero a los datos que se van a anexar al archivo.</span><span class="sxs-lookup"><span data-stu-id="6f3db-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="6f3db-122">Value</span><span class="sxs-lookup"><span data-stu-id="6f3db-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="6f3db-123">Significado</span><span class="sxs-lookup"><span data-stu-id="6f3db-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="6f3db-124"><dt>**TN**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="6f3db-125">1 byte</span><span class="sxs-lookup"><span data-stu-id="6f3db-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="6f3db-126"><dt>**LN**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="6f3db-127">1 o 3 bytes</span><span class="sxs-lookup"><span data-stu-id="6f3db-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="6f3db-128"><dt>**datos**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="6f3db-129">LN bytes</span><span class="sxs-lookup"><span data-stu-id="6f3db-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="6f3db-130">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3db-131">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="6f3db-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6f3db-132">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="6f3db-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6f3db-133">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="6f3db-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f3db-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f3db-134">Return value</span></span>

<span data-ttu-id="6f3db-135">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6f3db-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6f3db-136">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6f3db-136">Return code</span></span>                                                                                   | <span data-ttu-id="6f3db-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f3db-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6f3db-138"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f3db-139">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f3db-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6f3db-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6f3db-141">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6f3db-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6f3db-142"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6f3db-143">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="6f3db-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6f3db-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f3db-145">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6f3db-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6f3db-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f3db-146">Remarks</span></span>

<span data-ttu-id="6f3db-147">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental leído.</span><span class="sxs-lookup"><span data-stu-id="6f3db-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="6f3db-148">Si se selecciona otro archivo elemental en el momento de emitir este comando, se puede procesar sin identificación del archivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="6f3db-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="6f3db-149">No se pueden leer los archivos elementales sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="6f3db-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="6f3db-150">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura de registro.</span><span class="sxs-lookup"><span data-stu-id="6f3db-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="6f3db-151">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="6f3db-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6f3db-152">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f3db-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6f3db-153">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6f3db-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3db-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f3db-154">Requirements</span></span>



| <span data-ttu-id="6f3db-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f3db-155">Requirement</span></span> | <span data-ttu-id="6f3db-156">Value</span><span class="sxs-lookup"><span data-stu-id="6f3db-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3db-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f3db-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3db-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f3db-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f3db-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3db-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f3db-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f3db-161">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6f3db-161">End of client support</span></span><br/>    | <span data-ttu-id="6f3db-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f3db-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6f3db-163">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6f3db-163">End of server support</span></span><br/>    | <span data-ttu-id="6f3db-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f3db-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6f3db-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f3db-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f3db-166"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f3db-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f3db-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f3db-168"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f3db-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f3db-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3db-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f3db-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f3db-171">IID</span><span class="sxs-lookup"><span data-stu-id="6f3db-171">IID</span></span><br/>                      | <span data-ttu-id="6f3db-172">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6f3db-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6f3db-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f3db-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3db-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6f3db-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="6f3db-175">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="6f3db-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="6f3db-176">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="6f3db-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="6f3db-177">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="6f3db-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
