---
description: Recupera el byte de estado SW1 de APDU de respuesta.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Método ISCardCmd:: get_ReplyStatusSW1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541827"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="daaff-103">ISCardCmd:: get \_ ReplyStatusSW1 (método)</span><span class="sxs-lookup"><span data-stu-id="daaff-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="daaff-104">\[El método **Get \_ ReplyStatusSW1** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="daaff-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="daaff-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="daaff-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="daaff-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="daaff-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="daaff-107">El método **Get \_ ReplyStatusSW1** recupera el byte de estado de APDU SW1 de [*respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="daaff-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="daaff-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daaff-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="daaff-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daaff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daaff-110">*pbySW1* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="daaff-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daaff-111">Puntero al byte que contiene el valor del byte SW1 en la devolución.</span><span class="sxs-lookup"><span data-stu-id="daaff-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daaff-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daaff-112">Return value</span></span>

<span data-ttu-id="daaff-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="daaff-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="daaff-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="daaff-114">Return code</span></span>                                                                                   | <span data-ttu-id="daaff-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="daaff-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="daaff-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="daaff-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="daaff-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="daaff-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="daaff-119">El parámetro *pbySW1* no es válido.</span><span class="sxs-lookup"><span data-stu-id="daaff-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="daaff-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="daaff-121">Se pasó un puntero no válido en *pbySW1*.</span><span class="sxs-lookup"><span data-stu-id="daaff-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="daaff-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="daaff-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="daaff-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="daaff-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daaff-124">Remarks</span></span>

<span data-ttu-id="daaff-125">El byte [*de estado de SW1 de APDU de respuesta*](../secgloss/r-gly.md) es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="daaff-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="daaff-126">Para recuperar el byte de estado de SW2 de APDU de respuesta, llame a [**Get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span><span class="sxs-lookup"><span data-stu-id="daaff-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="daaff-127">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="daaff-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="daaff-128">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="daaff-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="daaff-129">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="daaff-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="daaff-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="daaff-130">Examples</span></span>

<span data-ttu-id="daaff-131">En el ejemplo siguiente se muestra cómo recuperar el byte de estado SW1 de las [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="daaff-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="daaff-132">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="daaff-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="daaff-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daaff-133">Requirements</span></span>



| <span data-ttu-id="daaff-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="daaff-134">Requirement</span></span> | <span data-ttu-id="daaff-135">Value</span><span class="sxs-lookup"><span data-stu-id="daaff-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="daaff-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daaff-136">Minimum supported client</span></span><br/> | <span data-ttu-id="daaff-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="daaff-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="daaff-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="daaff-138">Minimum supported server</span></span><br/> | <span data-ttu-id="daaff-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="daaff-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="daaff-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="daaff-140">End of client support</span></span><br/>    | <span data-ttu-id="daaff-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="daaff-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="daaff-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="daaff-142">End of server support</span></span><br/>    | <span data-ttu-id="daaff-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="daaff-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="daaff-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daaff-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="daaff-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="daaff-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="daaff-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="daaff-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="daaff-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="daaff-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daaff-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daaff-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="daaff-150">IID</span><span class="sxs-lookup"><span data-stu-id="daaff-150">IID</span></span><br/>                      | <span data-ttu-id="daaff-151">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="daaff-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="daaff-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="daaff-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daaff-153">**obtener \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="daaff-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="daaff-154">**obtener \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="daaff-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="daaff-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="daaff-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
