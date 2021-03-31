---
description: El método WriteBinary crea un comando de unidad de datos de protocolo de aplicación (APDU) que escribe valores binarios en un archivo elemental.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816:: WriteBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000915"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="ef257-103">ISCardISO7816:: WriteBinary (método)</span><span class="sxs-lookup"><span data-stu-id="ef257-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="ef257-104">\[El método **WriteBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ef257-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ef257-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ef257-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef257-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ef257-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ef257-107">El método **WriteBinary** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que escribe valores binarios en un archivo elemental.</span><span class="sxs-lookup"><span data-stu-id="ef257-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="ef257-108">En función de los atributos de archivo, el comando realiza una de las operaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ef257-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="ef257-109">El OR lógico de los bits que ya están presentes en la tarjeta con los bits especificados en el comando APDU (el estado de borrado lógico de los bits del archivo es 0).</span><span class="sxs-lookup"><span data-stu-id="ef257-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="ef257-110">El AND lógico de los bits que ya están presentes en la tarjeta con los bits especificados en el comando APDU (el estado de borrado lógico de los bits del archivo es 1).</span><span class="sxs-lookup"><span data-stu-id="ef257-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="ef257-111">La escritura única en la tarjeta de los bits especificados en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="ef257-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="ef257-112">Cuando no se especifica ninguna indicación en el byte de codificación de datos, se aplica el comportamiento lógico OR.</span><span class="sxs-lookup"><span data-stu-id="ef257-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef257-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef257-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ef257-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef257-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef257-115">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef257-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef257-116">Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF).</span><span class="sxs-lookup"><span data-stu-id="ef257-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="ef257-117">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ef257-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="ef257-118">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ef257-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ef257-119">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef257-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef257-120">Desplazamiento a la ubicación de escritura desde el principio del archivo binario (EF).</span><span class="sxs-lookup"><span data-stu-id="ef257-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="ef257-121">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ef257-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="ef257-122">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a escribir en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ef257-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ef257-123">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef257-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef257-124">Puntero a la cadena de unidades de datos que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="ef257-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="ef257-125">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef257-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef257-126">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="ef257-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="ef257-127">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="ef257-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="ef257-128">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="ef257-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef257-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef257-129">Return value</span></span>

<span data-ttu-id="ef257-130">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ef257-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ef257-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ef257-131">Return code</span></span>                                                                                   | <span data-ttu-id="ef257-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef257-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ef257-133"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ef257-134">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef257-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ef257-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ef257-136">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="ef257-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ef257-137"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ef257-138">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="ef257-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="ef257-139"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ef257-140">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="ef257-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ef257-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef257-141">Remarks</span></span>

<span data-ttu-id="ef257-142">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="ef257-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="ef257-143">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="ef257-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="ef257-144">Cuando se ha aplicado una operación de escritura binaria a una unidad de datos de un EF de escritura de una sola vez, cualquier operación de escritura que se refiera a esta unidad de datos se anulará si el contenido de la unidad de datos o el indicador de estado borrado lógico (si existe) asociado a esta unidad de datos es diferente del estado de borrado lógico.</span><span class="sxs-lookup"><span data-stu-id="ef257-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="ef257-145">No se puede escribir en los archivos elementales sin una estructura transparente.</span><span class="sxs-lookup"><span data-stu-id="ef257-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="ef257-146">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.</span><span class="sxs-lookup"><span data-stu-id="ef257-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="ef257-147">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="ef257-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="ef257-148">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef257-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ef257-149">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ef257-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef257-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef257-150">Requirements</span></span>



| <span data-ttu-id="ef257-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef257-151">Requirement</span></span> | <span data-ttu-id="ef257-152">Value</span><span class="sxs-lookup"><span data-stu-id="ef257-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef257-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef257-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ef257-154">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ef257-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef257-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef257-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ef257-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef257-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef257-157">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ef257-157">End of client support</span></span><br/>    | <span data-ttu-id="ef257-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef257-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ef257-159">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ef257-159">End of server support</span></span><br/>    | <span data-ttu-id="ef257-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef257-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ef257-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef257-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef257-162"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef257-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ef257-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef257-164"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef257-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef257-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef257-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef257-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef257-167">IID</span><span class="sxs-lookup"><span data-stu-id="ef257-167">IID</span></span><br/>                      | <span data-ttu-id="ef257-168">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ef257-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ef257-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef257-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef257-170">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="ef257-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="ef257-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="ef257-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="ef257-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="ef257-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="ef257-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="ef257-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
