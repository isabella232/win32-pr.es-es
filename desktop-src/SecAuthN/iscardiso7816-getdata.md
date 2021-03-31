---
description: El método GetData crea un comando de unidad de datos de protocolo de aplicación (APDU) que recupera un único objeto de datos primitivo o un conjunto de objetos de datos (contenidos en un objeto de datos construido), dependiendo del tipo de archivo seleccionado.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816:: GetData (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815819"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="d856f-103">ISCardISO7816:: GetData (método)</span><span class="sxs-lookup"><span data-stu-id="d856f-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="d856f-104">\[El método **GetData** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d856f-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d856f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d856f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d856f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d856f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d856f-107">El método **GetData** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que recupera un único objeto de datos primitivo o un conjunto de objetos de datos (contenidos en un objeto de datos construido), dependiendo del tipo de archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d856f-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="d856f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d856f-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="d856f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d856f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d856f-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d856f-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d856f-111">Parámetros.</span><span class="sxs-lookup"><span data-stu-id="d856f-111">Parameters.</span></span>



| <span data-ttu-id="d856f-112">Value</span><span class="sxs-lookup"><span data-stu-id="d856f-112">Value</span></span>                                                                                  | <span data-ttu-id="d856f-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d856f-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d856f-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="d856f-115">RFU</span><span class="sxs-lookup"><span data-stu-id="d856f-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="d856f-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="d856f-117">Etiqueta BER-TLV (1 byte) en P2</span><span class="sxs-lookup"><span data-stu-id="d856f-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="d856f-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="d856f-119">Datos de aplicación (codificación propietaria)</span><span class="sxs-lookup"><span data-stu-id="d856f-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="d856f-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="d856f-121">Etiqueta SIMPLE-TLV en P2</span><span class="sxs-lookup"><span data-stu-id="d856f-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="d856f-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="d856f-123">RFU</span><span class="sxs-lookup"><span data-stu-id="d856f-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="d856f-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="d856f-125">Etiqueta BER-TLV (2 bytes) en P1-P2</span><span class="sxs-lookup"><span data-stu-id="d856f-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="d856f-126">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d856f-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d856f-127">Parámetros.</span><span class="sxs-lookup"><span data-stu-id="d856f-127">Parameters.</span></span>



| <span data-ttu-id="d856f-128">Value</span><span class="sxs-lookup"><span data-stu-id="d856f-128">Value</span></span>                                                                                  | <span data-ttu-id="d856f-129">Significado</span><span class="sxs-lookup"><span data-stu-id="d856f-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d856f-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="d856f-131">RFU</span><span class="sxs-lookup"><span data-stu-id="d856f-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="d856f-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="d856f-133">Etiqueta BER-TLV (1 byte) en P2</span><span class="sxs-lookup"><span data-stu-id="d856f-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="d856f-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="d856f-135">Datos de aplicación (codificación propietaria)</span><span class="sxs-lookup"><span data-stu-id="d856f-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="d856f-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="d856f-137">Etiqueta SIMPLE-TLV en P2</span><span class="sxs-lookup"><span data-stu-id="d856f-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="d856f-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="d856f-139">RFU</span><span class="sxs-lookup"><span data-stu-id="d856f-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="d856f-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="d856f-141">Etiqueta BER-TLV (2 bytes) en P1-P2</span><span class="sxs-lookup"><span data-stu-id="d856f-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="d856f-142">*lBytesToGet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d856f-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d856f-143">Número de bytes esperados en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d856f-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="d856f-144">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d856f-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d856f-145">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="d856f-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="d856f-146">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="d856f-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="d856f-147">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="d856f-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d856f-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d856f-148">Return value</span></span>

<span data-ttu-id="d856f-149">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d856f-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d856f-150">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d856f-150">Return code</span></span>                                                                                   | <span data-ttu-id="d856f-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="d856f-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d856f-152"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d856f-153">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d856f-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d856f-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d856f-155">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d856f-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d856f-156"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d856f-157">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="d856f-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d856f-158"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d856f-159">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d856f-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d856f-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d856f-160">Remarks</span></span>

<span data-ttu-id="d856f-161">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está leyendo.</span><span class="sxs-lookup"><span data-stu-id="d856f-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="d856f-162">Las condiciones de seguridad dependen de la Directiva de la tarjeta y se pueden manipular a través de [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), etc.</span><span class="sxs-lookup"><span data-stu-id="d856f-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="d856f-163">Para seleccionar un archivo, llame a [**SelectFile**](iscardiso7816-selectfile.md).</span><span class="sxs-lookup"><span data-stu-id="d856f-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="d856f-164">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="d856f-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="d856f-165">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d856f-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d856f-166">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d856f-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d856f-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d856f-167">Requirements</span></span>



| <span data-ttu-id="d856f-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="d856f-168">Requirement</span></span> | <span data-ttu-id="d856f-169">Value</span><span class="sxs-lookup"><span data-stu-id="d856f-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d856f-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d856f-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d856f-171">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d856f-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d856f-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d856f-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d856f-173">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d856f-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d856f-174">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d856f-174">End of client support</span></span><br/>    | <span data-ttu-id="d856f-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d856f-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d856f-176">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d856f-176">End of server support</span></span><br/>    | <span data-ttu-id="d856f-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d856f-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d856f-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d856f-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="d856f-179"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d856f-180">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d856f-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="d856f-181"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d856f-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d856f-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d856f-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d856f-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d856f-184">IID</span><span class="sxs-lookup"><span data-stu-id="d856f-184">IID</span></span><br/>                      | <span data-ttu-id="d856f-185">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d856f-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="d856f-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="d856f-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d856f-187">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="d856f-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="d856f-188">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="d856f-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="d856f-189">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="d856f-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="d856f-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="d856f-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="d856f-191">**PutData**</span><span class="sxs-lookup"><span data-stu-id="d856f-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="d856f-192">**SelectFile**</span><span class="sxs-lookup"><span data-stu-id="d856f-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
