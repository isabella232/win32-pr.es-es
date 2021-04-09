---
description: Recupera la palabra de estado de mensaje de APDU de respuesta.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Método ISCardCmd:: get_ReplyStatus (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154354"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="bea29-103">ISCardCmd:: get \_ ReplyStatus (método)</span><span class="sxs-lookup"><span data-stu-id="bea29-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="bea29-104">\[El método **Get \_ ReplyStatus** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bea29-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bea29-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bea29-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bea29-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="bea29-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bea29-107">El método **Get \_ ReplyStatus** recupera la palabra [*de estado de mensaje de APDU de respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bea29-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea29-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea29-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bea29-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bea29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea29-110">*pwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bea29-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bea29-111">Puntero a la palabra que es el estado de la devolución.</span><span class="sxs-lookup"><span data-stu-id="bea29-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea29-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bea29-112">Return value</span></span>

<span data-ttu-id="bea29-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="bea29-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bea29-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bea29-114">Return code</span></span>                                                                                   | <span data-ttu-id="bea29-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bea29-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="bea29-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bea29-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="bea29-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="bea29-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bea29-119">El parámetro *pwStatus* no es válido.</span><span class="sxs-lookup"><span data-stu-id="bea29-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="bea29-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bea29-121">Se pasó un puntero no válido en *pwStatus*.</span><span class="sxs-lookup"><span data-stu-id="bea29-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="bea29-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bea29-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="bea29-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bea29-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea29-124">Remarks</span></span>

<span data-ttu-id="bea29-125">Para establecer la palabra de estado de mensaje de APDU de respuesta, llame a [**Put \_ ReplyStatus**](iscardcmd-put-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="bea29-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="bea29-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bea29-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="bea29-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bea29-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bea29-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bea29-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bea29-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bea29-129">Examples</span></span>

<span data-ttu-id="bea29-130">En el ejemplo siguiente se muestra cómo recuperar la palabra de estado del mensaje de [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bea29-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="bea29-131">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="bea29-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="bea29-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea29-132">Requirements</span></span>



| <span data-ttu-id="bea29-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea29-133">Requirement</span></span> | <span data-ttu-id="bea29-134">Value</span><span class="sxs-lookup"><span data-stu-id="bea29-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bea29-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea29-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bea29-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bea29-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bea29-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea29-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bea29-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bea29-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bea29-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bea29-139">End of client support</span></span><br/>    | <span data-ttu-id="bea29-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bea29-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bea29-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bea29-141">End of server support</span></span><br/>    | <span data-ttu-id="bea29-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bea29-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bea29-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea29-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea29-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bea29-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bea29-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="bea29-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bea29-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bea29-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bea29-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bea29-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bea29-149">IID</span><span class="sxs-lookup"><span data-stu-id="bea29-149">IID</span></span><br/>                      | <span data-ttu-id="bea29-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bea29-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bea29-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="bea29-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea29-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="bea29-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="bea29-153">**Put \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="bea29-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
