---
description: El método SelectFile crea un comando de unidad de datos de protocolo de aplicación (APDU) que establece un archivo elemental actual dentro de un canal lógico. Los comandos subsiguientes pueden hacer referencia implícitamente al archivo actual a través del canal lógico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816:: SelectFile (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277017"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="0c302-104">ISCardISO7816:: SelectFile (método)</span><span class="sxs-lookup"><span data-stu-id="0c302-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="0c302-105">\[El método **SelectFile** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0c302-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c302-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0c302-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c302-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0c302-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0c302-108">El método **SelectFile** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que establece un archivo elemental actual dentro de un canal lógico.</span><span class="sxs-lookup"><span data-stu-id="0c302-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="0c302-109">Los comandos subsiguientes pueden hacer referencia implícitamente al archivo actual a través del canal lógico.</span><span class="sxs-lookup"><span data-stu-id="0c302-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="0c302-110">La selección de un directorio (DF) en el almacén de almacén de la tarjeta (que puede ser la raíz (MF) del almacén de almacén) lo convierte en el DF actual.</span><span class="sxs-lookup"><span data-stu-id="0c302-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="0c302-111">Después de esta selección, se puede hacer referencia a un archivo elemental actual implícito a través de ese canal lógico.</span><span class="sxs-lookup"><span data-stu-id="0c302-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="0c302-112">Al seleccionar un archivo elemental, se establece el archivo seleccionado y su elemento primario como archivos actuales.</span><span class="sxs-lookup"><span data-stu-id="0c302-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="0c302-113">Después de la respuesta al restablecimiento, el MF se selecciona implícitamente a través del canal lógico básico, a menos que se especifique de manera diferente en los bytes históricos o en la cadena de datos inicial.</span><span class="sxs-lookup"><span data-stu-id="0c302-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c302-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c302-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="0c302-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c302-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c302-116">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c302-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c302-117">Control de selección.</span><span class="sxs-lookup"><span data-stu-id="0c302-117">Selection control.</span></span>



| <span data-ttu-id="0c302-118">P1 (byte superior de Word): 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="0c302-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="0c302-119">Significado</span><span class="sxs-lookup"><span data-stu-id="0c302-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="0c302-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c302-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="0c302-121">Seleccionar ID. de archivo</span><span class="sxs-lookup"><span data-stu-id="0c302-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="0c302-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c302-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="0c302-123">EF, DF o MF</span><span class="sxs-lookup"><span data-stu-id="0c302-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="0c302-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c302-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="0c302-125">DF secundario</span><span class="sxs-lookup"><span data-stu-id="0c302-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="0c302-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c302-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="0c302-127">EF en DF</span><span class="sxs-lookup"><span data-stu-id="0c302-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="0c302-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c302-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="0c302-129">DF primario del DF actual</span><span class="sxs-lookup"><span data-stu-id="0c302-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="0c302-130">Cuando P1 = 00, la tarjeta sabe bien debido a una codificación específica del identificador de archivo o debido al contexto de ejecución del comando si el archivo que se va a seleccionar es MF, un DF o un EF.</span><span class="sxs-lookup"><span data-stu-id="0c302-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="0c302-131">Cuando P1-P2 = 0000, si se proporciona un identificador de archivo, será único en los entornos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0c302-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="0c302-132">Elementos secundarios inmediatos del DF actual</span><span class="sxs-lookup"><span data-stu-id="0c302-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="0c302-133">DF primario</span><span class="sxs-lookup"><span data-stu-id="0c302-133">Parent DF</span></span>
-   <span data-ttu-id="0c302-134">Elementos secundarios inmediatos del DF primario</span><span class="sxs-lookup"><span data-stu-id="0c302-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="0c302-135">Si P1-P2 = 0000 y el campo de datos está vacío o es igual a 3F00, seleccione el MF.</span><span class="sxs-lookup"><span data-stu-id="0c302-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="0c302-136">Cuando P1 = 04, el campo de datos es un nombre de DF, posiblemente truncado.</span><span class="sxs-lookup"><span data-stu-id="0c302-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="0c302-137">Cuando se admiten, los comandos sucesivos con el mismo campo de datos deben seleccionar DFs cuyos nombres coincidan con el campo de datos (es decir, empezar con el campo de datos de comando).</span><span class="sxs-lookup"><span data-stu-id="0c302-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="0c302-138">Si la tarjeta acepta el comando con un campo de datos vacío, todos o un subconjunto del DFs se pueden seleccionar sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="0c302-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="0c302-139">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c302-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c302-140">Control de selección.</span><span class="sxs-lookup"><span data-stu-id="0c302-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="0c302-141">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c302-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c302-142">Datos de la operación si es necesario; en caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="0c302-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="0c302-143">Entre los tipos de datos que se pasan en este parámetro se incluyen:</span><span class="sxs-lookup"><span data-stu-id="0c302-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="0c302-144">IDENTIFICADOR de archivo</span><span class="sxs-lookup"><span data-stu-id="0c302-144">file ID</span></span>
-   <span data-ttu-id="0c302-145">Ruta de acceso del MF</span><span class="sxs-lookup"><span data-stu-id="0c302-145">path from the MF</span></span>
-   <span data-ttu-id="0c302-146">Ruta de acceso del DF actual</span><span class="sxs-lookup"><span data-stu-id="0c302-146">path from the current DF</span></span>
-   <span data-ttu-id="0c302-147">Nombre de DF</span><span class="sxs-lookup"><span data-stu-id="0c302-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="0c302-148">*lBytesToRead* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c302-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c302-149">Vacío (es decir, 0) o longitud máxima de los datos esperados en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c302-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="0c302-150">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0c302-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c302-151">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="0c302-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="0c302-152">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="0c302-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="0c302-153">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="0c302-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c302-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c302-154">Return value</span></span>

<span data-ttu-id="0c302-155">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0c302-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0c302-156">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c302-156">Return code</span></span>                                                                                   | <span data-ttu-id="0c302-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c302-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0c302-158"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0c302-159">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0c302-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0c302-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0c302-161">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="0c302-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0c302-162"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0c302-163">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="0c302-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0c302-164"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c302-165">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="0c302-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0c302-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c302-166">Remarks</span></span>

<span data-ttu-id="0c302-167">A menos que se especifique lo contrario, la ejecución correcta del comando encapsulado modifica el estado de seguridad de acuerdo con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="0c302-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="0c302-168">Cuando se cambia el archivo elemental actual, o cuando no hay ningún archivo elemental actual, se pierde el estado de seguridad específico de un archivo elemental actual anterior.</span><span class="sxs-lookup"><span data-stu-id="0c302-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="0c302-169">Cuando el directorio de almacén de información (DF) actual es descendiente de, o idéntico al DF anterior, se pierde el estado de seguridad específico del DF anterior actual.</span><span class="sxs-lookup"><span data-stu-id="0c302-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="0c302-170">Se mantiene el estado de seguridad común a todos los antecesores comunes del DF anterior y el nuevo actual.</span><span class="sxs-lookup"><span data-stu-id="0c302-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="0c302-171">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="0c302-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="0c302-172">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c302-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0c302-173">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0c302-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c302-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c302-174">Requirements</span></span>



| <span data-ttu-id="0c302-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c302-175">Requirement</span></span> | <span data-ttu-id="0c302-176">Value</span><span class="sxs-lookup"><span data-stu-id="0c302-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c302-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c302-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0c302-178">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0c302-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0c302-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c302-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0c302-180">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c302-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c302-181">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0c302-181">End of client support</span></span><br/>    | <span data-ttu-id="0c302-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c302-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0c302-183">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0c302-183">End of server support</span></span><br/>    | <span data-ttu-id="0c302-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c302-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0c302-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c302-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c302-186"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c302-187">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0c302-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c302-188"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0c302-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c302-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c302-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c302-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c302-191">IID</span><span class="sxs-lookup"><span data-stu-id="0c302-191">IID</span></span><br/>                      | <span data-ttu-id="0c302-192">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0c302-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0c302-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c302-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c302-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="0c302-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
