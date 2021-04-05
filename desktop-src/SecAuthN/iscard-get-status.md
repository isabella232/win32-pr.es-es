---
description: Recupera el estado actual de la tarjeta inteligente.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'Método ISCard:: get_Status (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279318"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="fbd9e-103">ISCard:: get \_ status (método)</span><span class="sxs-lookup"><span data-stu-id="fbd9e-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="fbd9e-104">\[El método **Get \_ status** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbd9e-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbd9e-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fbd9e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fbd9e-107">El método **Get \_ status** recupera el [*Estado*](../secgloss/s-gly.md) actual de la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fbd9e-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd9e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbd9e-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fbd9e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbd9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd9e-110">*pStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fbd9e-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd9e-111">Puntero a la variable de estado.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd9e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbd9e-112">Return value</span></span>

<span data-ttu-id="fbd9e-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fbd9e-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fbd9e-114">Return code</span></span>                                                                                  | <span data-ttu-id="fbd9e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbd9e-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="fbd9e-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fbd9e-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="fbd9e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fbd9e-119">El parámetro *pStatus* no es válido.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="fbd9e-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="fbd9e-121">Se pasó un puntero no válido en *pStatus*.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fbd9e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbd9e-122">Remarks</span></span>

<span data-ttu-id="fbd9e-123">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fbd9e-124">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fbd9e-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fbd9e-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fbd9e-125">Examples</span></span>

<span data-ttu-id="fbd9e-126">En el ejemplo siguiente se muestra cómo recuperar el estado actual de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fbd9e-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="fbd9e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbd9e-127">Requirements</span></span>



| <span data-ttu-id="fbd9e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd9e-128">Requirement</span></span> | <span data-ttu-id="fbd9e-129">Value</span><span class="sxs-lookup"><span data-stu-id="fbd9e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd9e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbd9e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd9e-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd9e-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fbd9e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbd9e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd9e-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd9e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbd9e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fbd9e-134">End of client support</span></span><br/>    | <span data-ttu-id="fbd9e-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbd9e-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fbd9e-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fbd9e-136">End of server support</span></span><br/>    | <span data-ttu-id="fbd9e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbd9e-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fbd9e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbd9e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbd9e-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbd9e-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fbd9e-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbd9e-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fbd9e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbd9e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbd9e-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbd9e-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbd9e-144">IID</span><span class="sxs-lookup"><span data-stu-id="fbd9e-144">IID</span></span><br/>                      | <span data-ttu-id="fbd9e-145">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fbd9e-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fbd9e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbd9e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd9e-147">**obtener \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="fbd9e-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="fbd9e-148">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="fbd9e-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="fbd9e-149">**obtener \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="fbd9e-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="fbd9e-150">**obtener \_ Protocolo**</span><span class="sxs-lookup"><span data-stu-id="fbd9e-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="fbd9e-151">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="fbd9e-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
