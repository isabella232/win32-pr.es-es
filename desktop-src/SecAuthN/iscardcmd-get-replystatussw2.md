---
description: Recupera el byte de estado SW2 de APDU de respuesta.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'Método ISCardCmd:: get_ReplyStatusSW2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154353"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="5f1cb-103">ISCardCmd:: get \_ ReplyStatusSW2 (método)</span><span class="sxs-lookup"><span data-stu-id="5f1cb-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="5f1cb-104">\[El método **Get \_ ReplyStatusSW2** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f1cb-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f1cb-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5f1cb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5f1cb-107">El método **Get \_ ReplyStatusSW2** recupera el byte de estado APDU SW2 de [*respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1cb-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f1cb-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="5f1cb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f1cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1cb-110">*pbySW2* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5f1cb-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1cb-111">Puntero al byte que contiene el valor del byte SW2 en la devolución.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1cb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f1cb-112">Return value</span></span>

<span data-ttu-id="5f1cb-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5f1cb-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5f1cb-114">Return code</span></span>                                                                                   | <span data-ttu-id="5f1cb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f1cb-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5f1cb-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5f1cb-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="5f1cb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5f1cb-119">*PbySW2* no es válido.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="5f1cb-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5f1cb-121">Se pasó un puntero no válido en *pbySW2*.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="5f1cb-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5f1cb-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="5f1cb-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="5f1cb-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f1cb-124">Remarks</span></span>

<span data-ttu-id="5f1cb-125">El byte de estado de SW2 de APDU de respuesta es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="5f1cb-126">Para recuperar el byte de estado de SW1 de APDU de respuesta, llame a [**Get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span><span class="sxs-lookup"><span data-stu-id="5f1cb-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="5f1cb-127">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="5f1cb-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="5f1cb-128">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f1cb-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5f1cb-129">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5f1cb-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5f1cb-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5f1cb-130">Examples</span></span>

<span data-ttu-id="5f1cb-131">En el ejemplo siguiente se muestra cómo recuperar el byte de estado SW2 de las [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5f1cb-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="5f1cb-132">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1cb-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5f1cb-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f1cb-133">Requirements</span></span>



| <span data-ttu-id="5f1cb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1cb-134">Requirement</span></span> | <span data-ttu-id="5f1cb-135">Value</span><span class="sxs-lookup"><span data-stu-id="5f1cb-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1cb-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1cb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1cb-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1cb-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f1cb-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1cb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1cb-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1cb-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f1cb-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5f1cb-140">End of client support</span></span><br/>    | <span data-ttu-id="5f1cb-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f1cb-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5f1cb-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5f1cb-142">End of server support</span></span><br/>    | <span data-ttu-id="5f1cb-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f1cb-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5f1cb-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f1cb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1cb-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f1cb-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5f1cb-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f1cb-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f1cb-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f1cb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f1cb-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f1cb-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f1cb-150">IID</span><span class="sxs-lookup"><span data-stu-id="5f1cb-150">IID</span></span><br/>                      | <span data-ttu-id="5f1cb-151">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5f1cb-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5f1cb-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f1cb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1cb-153">**obtener \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="5f1cb-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="5f1cb-154">**obtener \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="5f1cb-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="5f1cb-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="5f1cb-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
