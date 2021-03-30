---
description: El método GetProviderCardId recupera el identificador (GUID) del proveedor de servicios principal de la tarjeta inteligente especificada.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'ISCardDatabase:: GetProviderCardId (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816790"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="acef9-103">ISCardDatabase:: GetProviderCardId (método)</span><span class="sxs-lookup"><span data-stu-id="acef9-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="acef9-104">\[El método **GetProviderCardId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="acef9-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="acef9-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="acef9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="acef9-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="acef9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="acef9-107">El método **GetProviderCardId** recupera el identificador (GUID) del [*proveedor de servicios principal*](../secgloss/p-gly.md) de la [*tarjeta inteligente*](../secgloss/s-gly.md)especificada.</span><span class="sxs-lookup"><span data-stu-id="acef9-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="acef9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acef9-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="acef9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acef9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acef9-110">*bstrCardName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="acef9-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acef9-111">Nombre de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="acef9-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="acef9-112">*ppguidProviderId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acef9-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acef9-113">Puntero al identificador del proveedor de servicios primario (GUID) si es correcto; **Null** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="acef9-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acef9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acef9-114">Return value</span></span>

<span data-ttu-id="acef9-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="acef9-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="acef9-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="acef9-116">Return code</span></span>                                                                                   | <span data-ttu-id="acef9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="acef9-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="acef9-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="acef9-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="acef9-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="acef9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="acef9-121">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="acef9-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="acef9-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="acef9-123">Se pasó un puntero no válido en *ppguidProviderId*.</span><span class="sxs-lookup"><span data-stu-id="acef9-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="acef9-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="acef9-125">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="acef9-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="acef9-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acef9-126">Remarks</span></span>

<span data-ttu-id="acef9-127">Para enumerar las interfaces de la tarjeta inteligente, llame a [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span><span class="sxs-lookup"><span data-stu-id="acef9-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="acef9-128">Para recuperar todas las [*tarjetas inteligentes*](../secgloss/s-gly.md)conocidas, los [*lectores*](../secgloss/r-gly.md) y los [*grupos de lector*](../secgloss/r-gly.md) llaman a [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)y [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="acef9-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="acef9-129">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="acef9-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="acef9-130">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="acef9-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="acef9-131">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="acef9-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="acef9-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="acef9-132">Examples</span></span>

<span data-ttu-id="acef9-133">En el ejemplo siguiente se muestra cómo recuperar el identificador del proveedor de servicios principal de la tarjeta inteligente especificada.</span><span class="sxs-lookup"><span data-stu-id="acef9-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="acef9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acef9-134">Requirements</span></span>



| <span data-ttu-id="acef9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="acef9-135">Requirement</span></span> | <span data-ttu-id="acef9-136">Value</span><span class="sxs-lookup"><span data-stu-id="acef9-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acef9-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acef9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="acef9-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="acef9-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="acef9-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acef9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="acef9-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="acef9-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acef9-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="acef9-141">End of client support</span></span><br/>    | <span data-ttu-id="acef9-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="acef9-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="acef9-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="acef9-143">End of server support</span></span><br/>    | <span data-ttu-id="acef9-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acef9-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="acef9-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acef9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="acef9-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="acef9-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="acef9-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="acef9-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="acef9-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acef9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acef9-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acef9-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="acef9-151">IID</span><span class="sxs-lookup"><span data-stu-id="acef9-151">IID</span></span><br/>                      | <span data-ttu-id="acef9-152">IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="acef9-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="acef9-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="acef9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acef9-154">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="acef9-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="acef9-155">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="acef9-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="acef9-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="acef9-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="acef9-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="acef9-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="acef9-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="acef9-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
