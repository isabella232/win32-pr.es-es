---
description: El método Encapsulate encapsula la unidad de datos de protocolo de aplicación de comandos (APDU) determinada en otra APDU de comando para su transmisión a una tarjeta inteligente.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'ISCardCmd:: Encapsulate (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652917"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="2db67-103">ISCardCmd:: Encapsulate (método)</span><span class="sxs-lookup"><span data-stu-id="2db67-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="2db67-104">\[El método **Encapsulate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2db67-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2db67-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2db67-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2db67-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2db67-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2db67-107">El método **Encapsulate** encapsula la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de comandos (APDU) determinada en otra APDU de comando para su transmisión a una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2db67-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2db67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2db67-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="2db67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2db67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db67-110">*pApdu* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2db67-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db67-111">Puntero a la APDU que se va a encapsular.</span><span class="sxs-lookup"><span data-stu-id="2db67-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="2db67-112">*ApduType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2db67-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db67-113">ISO 7816-4 Case for [*T = 0*](../secgloss/t-gly.md) transmisiones.</span><span class="sxs-lookup"><span data-stu-id="2db67-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="2db67-114">**\_Caso ISO \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2db67-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="2db67-115">**\_Caso ISO \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2db67-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="2db67-116">**\_Caso \_ 3 de ISO**</span><span class="sxs-lookup"><span data-stu-id="2db67-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="2db67-117">**ISO \_ Case \_ 4**</span><span class="sxs-lookup"><span data-stu-id="2db67-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db67-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2db67-118">Return value</span></span>

<span data-ttu-id="2db67-119">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2db67-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2db67-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2db67-120">Return code</span></span>                                                                                   | <span data-ttu-id="2db67-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db67-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2db67-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2db67-123">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2db67-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="2db67-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2db67-125">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2db67-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="2db67-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2db67-127">Se pasó un puntero no válido en *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="2db67-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="2db67-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2db67-129">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="2db67-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="2db67-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2db67-130">Remarks</span></span>

<span data-ttu-id="2db67-131">Para compilar una APDU de comando, llame a [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="2db67-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="2db67-132">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="2db67-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="2db67-133">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2db67-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2db67-134">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2db67-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2db67-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2db67-135">Examples</span></span>

<span data-ttu-id="2db67-136">En el ejemplo siguiente se muestra cómo encapsular una APDU de comando.</span><span class="sxs-lookup"><span data-stu-id="2db67-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="2db67-137">En el ejemplo se da por supuesto que pIByteApdu es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2db67-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2db67-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2db67-138">Requirements</span></span>



| <span data-ttu-id="2db67-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db67-139">Requirement</span></span> | <span data-ttu-id="2db67-140">Value</span><span class="sxs-lookup"><span data-stu-id="2db67-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db67-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2db67-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2db67-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2db67-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2db67-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2db67-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2db67-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2db67-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2db67-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2db67-145">End of client support</span></span><br/>    | <span data-ttu-id="2db67-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2db67-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2db67-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2db67-147">End of server support</span></span><br/>    | <span data-ttu-id="2db67-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2db67-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2db67-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2db67-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db67-150"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2db67-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2db67-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="2db67-152"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2db67-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2db67-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db67-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db67-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2db67-155">IID</span><span class="sxs-lookup"><span data-stu-id="2db67-155">IID</span></span><br/>                      | <span data-ttu-id="2db67-156">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2db67-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2db67-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="2db67-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db67-158">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="2db67-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="2db67-159">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="2db67-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
