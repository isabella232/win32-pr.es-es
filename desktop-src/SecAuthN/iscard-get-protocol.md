---
description: Recupera el identificador del protocolo actualmente en uso en la tarjeta inteligente.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Método ISCard:: get_Protocol (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361209"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="4755d-103">ISCard:: get ( \_ método de protocolo)</span><span class="sxs-lookup"><span data-stu-id="4755d-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="4755d-104">\[El método **Get \_ Protocol** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="4755d-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4755d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4755d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4755d-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4755d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4755d-107">El método **Get \_ Protocol** recupera el identificador del protocolo actualmente en uso en la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4755d-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4755d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4755d-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="4755d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4755d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4755d-110">*pProtocol* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4755d-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4755d-111">Puntero al identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="4755d-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4755d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4755d-112">Return value</span></span>

<span data-ttu-id="4755d-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4755d-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4755d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4755d-114">Return code</span></span>                                                                                  | <span data-ttu-id="4755d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4755d-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="4755d-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4755d-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="4755d-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="4755d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4755d-119">El parámetro *pProtocol* no es válido.</span><span class="sxs-lookup"><span data-stu-id="4755d-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4755d-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4755d-121">Se pasó un puntero no válido en *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="4755d-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4755d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4755d-122">Remarks</span></span>

<span data-ttu-id="4755d-123">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4755d-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4755d-124">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4755d-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4755d-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4755d-125">Examples</span></span>

<span data-ttu-id="4755d-126">En el ejemplo siguiente se muestra cómo recuperar el identificador del protocolo actualmente en uso en la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="4755d-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="4755d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4755d-127">Requirements</span></span>



| <span data-ttu-id="4755d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4755d-128">Requirement</span></span> | <span data-ttu-id="4755d-129">Value</span><span class="sxs-lookup"><span data-stu-id="4755d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4755d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4755d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4755d-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4755d-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4755d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4755d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4755d-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4755d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4755d-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4755d-134">End of client support</span></span><br/>    | <span data-ttu-id="4755d-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4755d-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4755d-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4755d-136">End of server support</span></span><br/>    | <span data-ttu-id="4755d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4755d-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4755d-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4755d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4755d-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="4755d-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4755d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4755d-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4755d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4755d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4755d-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4755d-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4755d-144">IID</span><span class="sxs-lookup"><span data-stu-id="4755d-144">IID</span></span><br/>                      | <span data-ttu-id="4755d-145">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4755d-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4755d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4755d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4755d-147">**obtener \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="4755d-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="4755d-148">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="4755d-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="4755d-149">**obtener \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="4755d-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="4755d-150">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="4755d-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="4755d-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="4755d-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
