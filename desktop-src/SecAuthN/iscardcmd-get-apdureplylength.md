---
description: Determina la longitud (en bytes) de la unidad de datos del Protocolo de aplicación (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'Método ISCardCmd:: get_ApduReplyLength (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279317"
---
# <a name="iscardcmdget_apdureplylength-method"></a><span data-ttu-id="a86fc-103">ISCardCmd:: get \_ ApduReplyLength (método)</span><span class="sxs-lookup"><span data-stu-id="a86fc-103">ISCardCmd::get\_ApduReplyLength method</span></span>

<span data-ttu-id="a86fc-104">\[El método **Get \_ ApduReplyLength** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a86fc-104">\[The **get\_ApduReplyLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a86fc-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a86fc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a86fc-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a86fc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a86fc-107">El método **Get \_ ApduReplyLength** determina la longitud (en bytes) de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a86fc-107">The **get\_ApduReplyLength** method determines the length (in bytes) of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a86fc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a86fc-108">Syntax</span></span>


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="a86fc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a86fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a86fc-110">*plSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a86fc-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a86fc-111">Puntero al tamaño del mensaje APDU de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a86fc-111">Pointer to the size of the reply APDU message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a86fc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a86fc-112">Return value</span></span>

<span data-ttu-id="a86fc-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a86fc-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a86fc-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a86fc-114">Return code</span></span>                                                                                   | <span data-ttu-id="a86fc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a86fc-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a86fc-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a86fc-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a86fc-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a86fc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a86fc-119">El parámetro *plSize* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a86fc-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a86fc-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a86fc-121">Se pasó un puntero no válido en *plSize*.</span><span class="sxs-lookup"><span data-stu-id="a86fc-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="a86fc-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a86fc-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="a86fc-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a86fc-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a86fc-124">Remarks</span></span>

<span data-ttu-id="a86fc-125">Para obtener una APDU de respuesta existente, llame a [**Get \_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="a86fc-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="a86fc-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a86fc-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a86fc-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a86fc-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a86fc-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a86fc-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a86fc-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a86fc-129">Examples</span></span>

<span data-ttu-id="a86fc-130">En el ejemplo siguiente se muestra cómo recuperar la longitud de las [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a86fc-130">The following example shows how to retrieve the length of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="a86fc-131">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a86fc-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="a86fc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a86fc-132">Requirements</span></span>



| <span data-ttu-id="a86fc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86fc-133">Requirement</span></span> | <span data-ttu-id="a86fc-134">Value</span><span class="sxs-lookup"><span data-stu-id="a86fc-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a86fc-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86fc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a86fc-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a86fc-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a86fc-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86fc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a86fc-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a86fc-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a86fc-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a86fc-139">End of client support</span></span><br/>    | <span data-ttu-id="a86fc-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a86fc-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a86fc-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a86fc-141">End of server support</span></span><br/>    | <span data-ttu-id="a86fc-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a86fc-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a86fc-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a86fc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a86fc-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a86fc-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a86fc-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a86fc-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a86fc-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a86fc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a86fc-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a86fc-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a86fc-149">IID</span><span class="sxs-lookup"><span data-stu-id="a86fc-149">IID</span></span><br/>                      | <span data-ttu-id="a86fc-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a86fc-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a86fc-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a86fc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86fc-152">**obtener \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="a86fc-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="a86fc-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a86fc-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a86fc-154">**Put \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="a86fc-154">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
