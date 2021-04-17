---
description: El método UpdateBinary crea un comando de unidad de datos de protocolo de aplicación (APDU) que actualiza los bits presentes en un archivo elemental con los bits especificados en el comando APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'ISCardISO7816:: UpdateBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652766"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="574ea-103">ISCardISO7816:: UpdateBinary (método)</span><span class="sxs-lookup"><span data-stu-id="574ea-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="574ea-104">\[El método **UpdateBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="574ea-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="574ea-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="574ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="574ea-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="574ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="574ea-107">El método **UpdateBinary** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que actualiza los bits presentes en un archivo elemental con los bits especificados en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="574ea-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="574ea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="574ea-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="574ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="574ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="574ea-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="574ea-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="574ea-111">Desplazamiento a la ubicación de escritura (actualización) en el binario desde el inicio del archivo binario.</span><span class="sxs-lookup"><span data-stu-id="574ea-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="574ea-112">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a actualizar en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="574ea-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="574ea-113">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a actualizar en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="574ea-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="574ea-114">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="574ea-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="574ea-115">Desplazamiento a la ubicación de escritura (actualización) en el binario desde el inicio del archivo binario.</span><span class="sxs-lookup"><span data-stu-id="574ea-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="574ea-116">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a actualizar en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="574ea-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="574ea-117">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a actualizar en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="574ea-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="574ea-118">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="574ea-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="574ea-119">Puntero a la cadena de unidades de datos que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="574ea-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="574ea-120">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="574ea-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="574ea-121">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="574ea-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="574ea-122">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="574ea-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="574ea-123">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="574ea-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="574ea-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="574ea-124">Return value</span></span>

<span data-ttu-id="574ea-125">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="574ea-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="574ea-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="574ea-126">Return code</span></span>                                                                                   | <span data-ttu-id="574ea-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="574ea-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="574ea-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="574ea-129">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="574ea-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="574ea-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="574ea-131">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="574ea-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="574ea-132"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="574ea-133">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="574ea-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="574ea-134"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="574ea-135">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="574ea-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="574ea-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="574ea-136">Remarks</span></span>

<span data-ttu-id="574ea-137">El comando encapsulado solo puede realizarse si el estado de seguridad de la tarjeta inteligente cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="574ea-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="574ea-138">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="574ea-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="574ea-139">Los archivos elementales sin una estructura transparente no se pueden borrar.</span><span class="sxs-lookup"><span data-stu-id="574ea-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="574ea-140">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.</span><span class="sxs-lookup"><span data-stu-id="574ea-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="574ea-141">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="574ea-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="574ea-142">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="574ea-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="574ea-143">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="574ea-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="574ea-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="574ea-144">Requirements</span></span>



| <span data-ttu-id="574ea-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="574ea-145">Requirement</span></span> | <span data-ttu-id="574ea-146">Value</span><span class="sxs-lookup"><span data-stu-id="574ea-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="574ea-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="574ea-147">Minimum supported client</span></span><br/> | <span data-ttu-id="574ea-148">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="574ea-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="574ea-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="574ea-149">Minimum supported server</span></span><br/> | <span data-ttu-id="574ea-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="574ea-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="574ea-151">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="574ea-151">End of client support</span></span><br/>    | <span data-ttu-id="574ea-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="574ea-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="574ea-153">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="574ea-153">End of server support</span></span><br/>    | <span data-ttu-id="574ea-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="574ea-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="574ea-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="574ea-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="574ea-156"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="574ea-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="574ea-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="574ea-158"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="574ea-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="574ea-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="574ea-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="574ea-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="574ea-161">IID</span><span class="sxs-lookup"><span data-stu-id="574ea-161">IID</span></span><br/>                      | <span data-ttu-id="574ea-162">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="574ea-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="574ea-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="574ea-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="574ea-164">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="574ea-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="574ea-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="574ea-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="574ea-166">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="574ea-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="574ea-167">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="574ea-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
