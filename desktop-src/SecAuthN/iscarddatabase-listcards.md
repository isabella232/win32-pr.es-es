---
description: El método ListCards recupera todos los nombres de tarjetas inteligentes que coinciden con los identificadores de interfaz especificados (GUID), la cadena ATR especificada o ambos.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'ISCardDatabase:: ListCards (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809913"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="e2730-103">ISCardDatabase:: ListCards (método)</span><span class="sxs-lookup"><span data-stu-id="e2730-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="e2730-104">\[El método **ListCards** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e2730-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e2730-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e2730-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e2730-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e2730-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e2730-107">El método **ListCards** recupera todos los nombres de tarjetas inteligentes que coinciden con los identificadores de interfaz especificados (GUID), la [*cadena ATR*](../secgloss/a-gly.md)especificada o ambos.</span><span class="sxs-lookup"><span data-stu-id="e2730-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2730-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2730-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="e2730-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2730-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2730-110">*pAtr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2730-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2730-111">Puntero a una cadena ATR de [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e2730-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="e2730-112">La cadena ATR se debe empaquetar en un [**IByteBuffer**](ibytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e2730-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2730-113">*pInterfaceGuids* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2730-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2730-114">Puntero a una matriz SAFEARRAY de identificadores de interfaz COM (GUID) en formato BSTR.</span><span class="sxs-lookup"><span data-stu-id="e2730-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="e2730-115">*localeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2730-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2730-116">Identificador de localización de idioma.</span><span class="sxs-lookup"><span data-stu-id="e2730-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e2730-117">*ppCardNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e2730-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2730-118">Puntero a un SAFEARRAY de BSTR que contiene los nombres de las tarjetas inteligentes que cumplen los parámetros de búsqueda si se realizan correctamente; **Null** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="e2730-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2730-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2730-119">Return value</span></span>

<span data-ttu-id="e2730-120">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="e2730-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e2730-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e2730-121">Return code</span></span>                                                                                   | <span data-ttu-id="e2730-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2730-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e2730-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e2730-124">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2730-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e2730-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e2730-126">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e2730-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e2730-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e2730-128">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="e2730-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e2730-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e2730-130">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="e2730-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e2730-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2730-131">Remarks</span></span>

<span data-ttu-id="e2730-132">Para recuperar todos los [*lectores o lectores*](../secgloss/r-gly.md) [*conocidos, llame*](../secgloss/r-gly.md)a [**ListReaders**](iscarddatabase-listreaders.md) o [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2730-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="e2730-133">Para recuperar el [*servicio principal*](../secgloss/p-gly.md) o las interfaces de una tarjeta específica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e2730-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="e2730-134">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="e2730-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="e2730-135">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2730-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e2730-136">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e2730-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e2730-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e2730-137">Examples</span></span>

<span data-ttu-id="e2730-138">En el ejemplo siguiente se muestra cómo recuperar los nombres de las tarjetas inteligentes que coinciden con la cadena ATR especificada.</span><span class="sxs-lookup"><span data-stu-id="e2730-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e2730-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2730-139">Requirements</span></span>



| <span data-ttu-id="e2730-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2730-140">Requirement</span></span> | <span data-ttu-id="e2730-141">Value</span><span class="sxs-lookup"><span data-stu-id="e2730-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2730-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2730-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e2730-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e2730-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e2730-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2730-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e2730-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2730-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2730-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e2730-146">End of client support</span></span><br/>    | <span data-ttu-id="e2730-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2730-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e2730-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e2730-148">End of server support</span></span><br/>    | <span data-ttu-id="e2730-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2730-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e2730-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2730-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2730-151"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2730-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e2730-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2730-153"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2730-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2730-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2730-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2730-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2730-156">IID</span><span class="sxs-lookup"><span data-stu-id="e2730-156">IID</span></span><br/>                      | <span data-ttu-id="e2730-157">IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e2730-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e2730-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2730-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2730-159">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="e2730-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="e2730-160">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="e2730-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="e2730-161">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="e2730-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="e2730-162">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="e2730-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="e2730-163">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="e2730-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
