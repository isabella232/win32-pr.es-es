---
description: Recupera la dirección de nodo (NAD) utilizada por la tarjeta inteligente en el mensaje de respuesta.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Método ISCardCmd:: get_ReplyNad (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154355"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="277eb-103">ISCardCmd:: get \_ ReplyNad (método)</span><span class="sxs-lookup"><span data-stu-id="277eb-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="277eb-104">\[El método **Get \_ ReplyNad** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="277eb-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="277eb-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="277eb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="277eb-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="277eb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="277eb-107">El método **Get \_ ReplyNad** recupera la dirección de nodo (NAD) utilizada por la [*tarjeta inteligente*](../secgloss/s-gly.md) en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="277eb-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="277eb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="277eb-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="277eb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="277eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277eb-110">*pbNad* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="277eb-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="277eb-111">Puntero al byte que contiene el NAD utilizado por el mensaje de respuesta, en la devolución.</span><span class="sxs-lookup"><span data-stu-id="277eb-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277eb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="277eb-112">Return value</span></span>

<span data-ttu-id="277eb-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="277eb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="277eb-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="277eb-114">Return code</span></span>                                                                                    | <span data-ttu-id="277eb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="277eb-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="277eb-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="277eb-117">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="277eb-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="277eb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="277eb-119">El parámetro *pbNad* no es válido.</span><span class="sxs-lookup"><span data-stu-id="277eb-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="277eb-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="277eb-121">Las llamadas internas no pudieron recuperar la información de NAD.</span><span class="sxs-lookup"><span data-stu-id="277eb-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="277eb-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="277eb-122">Remarks</span></span>

<span data-ttu-id="277eb-123">Además de los códigos de error COM enumerados anteriormente, este método puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="277eb-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="277eb-124">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="277eb-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="277eb-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="277eb-125">Examples</span></span>

<span data-ttu-id="277eb-126">En el ejemplo siguiente se muestra cómo recuperar la dirección de nodo (NAD) utilizada por la [*tarjeta inteligente*](../secgloss/s-gly.md) en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="277eb-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="277eb-127">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="277eb-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="277eb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="277eb-128">Requirements</span></span>



| <span data-ttu-id="277eb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="277eb-129">Requirement</span></span> | <span data-ttu-id="277eb-130">Value</span><span class="sxs-lookup"><span data-stu-id="277eb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="277eb-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="277eb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="277eb-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="277eb-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="277eb-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="277eb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="277eb-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="277eb-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="277eb-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="277eb-135">End of client support</span></span><br/>    | <span data-ttu-id="277eb-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="277eb-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="277eb-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="277eb-137">End of server support</span></span><br/>    | <span data-ttu-id="277eb-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="277eb-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="277eb-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="277eb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="277eb-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="277eb-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="277eb-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="277eb-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="277eb-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="277eb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="277eb-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="277eb-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="277eb-145">IID</span><span class="sxs-lookup"><span data-stu-id="277eb-145">IID</span></span><br/>                      | <span data-ttu-id="277eb-146">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="277eb-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="277eb-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="277eb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277eb-148">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="277eb-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
