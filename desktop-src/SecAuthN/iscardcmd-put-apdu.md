---
description: Copia la unidad de datos de protocolo de aplicación (APDU) del objeto IByteBuffer (IStream) en las APDU ajustadas en este objeto de interfaz.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'ISCardCmd: método de ut_Apdu de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001161"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="7ba4f-103">ISCardCmd: \_ método Apdu:p UT</span><span class="sxs-lookup"><span data-stu-id="7ba4f-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="7ba4f-104">\[El método **Put \_ APDU** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ba4f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7ba4f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7ba4f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7ba4f-107">El **método put \_ APDU** copia la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) del objeto [**IBYTEBUFFER**](ibytebuffer.md) (**IStream**) en las APDU ajustadas en este objeto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba4f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ba4f-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="7ba4f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ba4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba4f-110">*pApdu* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7ba4f-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba4f-111">Puntero a la APDU ISO 7816-4 en la que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba4f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ba4f-112">Return value</span></span>

<span data-ttu-id="7ba4f-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7ba4f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7ba4f-114">Return code</span></span>                                                                                   | <span data-ttu-id="7ba4f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ba4f-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7ba4f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7ba4f-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="7ba4f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7ba4f-119">El parámetro *pApdu* no es válido.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="7ba4f-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7ba4f-121">Se pasó un puntero no válido en *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="7ba4f-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7ba4f-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7ba4f-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="7ba4f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ba4f-124">Remarks</span></span>

<span data-ttu-id="7ba4f-125">Para recuperar las APDU sin formato del búfer de bytes asignado a través de una **IStream** que contiene el mensaje APDU, llame a [**Get \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="7ba4f-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="7ba4f-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7ba4f-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7ba4f-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7ba4f-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7ba4f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7ba4f-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7ba4f-129">Examples</span></span>

<span data-ttu-id="7ba4f-130">En el ejemplo siguiente se muestra cómo copiar un APDU de un objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) en las APDU contenidas en un objeto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7ba4f-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="7ba4f-131">En el ejemplo se da por supuesto que pIByteApdu es un puntero válido a una instancia de **IByteBuffer** y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba4f-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7ba4f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ba4f-132">Requirements</span></span>



| <span data-ttu-id="7ba4f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba4f-133">Requirement</span></span> | <span data-ttu-id="7ba4f-134">Value</span><span class="sxs-lookup"><span data-stu-id="7ba4f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba4f-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ba4f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba4f-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7ba4f-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7ba4f-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ba4f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba4f-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ba4f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ba4f-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7ba4f-139">End of client support</span></span><br/>    | <span data-ttu-id="7ba4f-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ba4f-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7ba4f-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7ba4f-141">End of server support</span></span><br/>    | <span data-ttu-id="7ba4f-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ba4f-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7ba4f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ba4f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ba4f-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ba4f-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7ba4f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ba4f-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7ba4f-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ba4f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba4f-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba4f-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ba4f-149">IID</span><span class="sxs-lookup"><span data-stu-id="7ba4f-149">IID</span></span><br/>                      | <span data-ttu-id="7ba4f-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7ba4f-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7ba4f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ba4f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba4f-152">**obtener \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="7ba4f-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="7ba4f-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="7ba4f-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
