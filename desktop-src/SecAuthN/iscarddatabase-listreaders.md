---
description: El método ListReaders recupera los nombres de los lectores de tarjetas inteligentes registrados en la base de datos de tarjetas inteligentes.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'ISCardDatabase:: ListReaders (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652425"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="6189b-103">ISCardDatabase:: ListReaders (método)</span><span class="sxs-lookup"><span data-stu-id="6189b-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="6189b-104">\[El método **ListReaders** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6189b-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6189b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6189b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6189b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6189b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6189b-107">El método **ListReaders** recupera los nombres de los [*lectores*](../secgloss/r-gly.md) de tarjetas inteligentes registrados en la [*base de datos de tarjetas inteligentes*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6189b-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6189b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6189b-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="6189b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6189b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6189b-110">*localeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6189b-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6189b-111">IDENTIFICADOR de localización de idioma.</span><span class="sxs-lookup"><span data-stu-id="6189b-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="6189b-112">*ppReaders* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6189b-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6189b-113">Puntero a un SAFEARRAY de BSTR que contiene los nombres de los lectores de tarjetas inteligentes si se realiza correctamente; **Null** si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="6189b-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6189b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6189b-114">Return value</span></span>

<span data-ttu-id="6189b-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6189b-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6189b-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6189b-116">Return code</span></span>                                                                                   | <span data-ttu-id="6189b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6189b-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6189b-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6189b-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6189b-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="6189b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6189b-121">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6189b-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="6189b-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6189b-123">Se pasó un puntero no válido en *ppReaders*.</span><span class="sxs-lookup"><span data-stu-id="6189b-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="6189b-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6189b-125">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6189b-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="6189b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6189b-126">Remarks</span></span>

<span data-ttu-id="6189b-127">Para recuperar todos los [*grupos de lectores*](../secgloss/r-gly.md)o [*tarjetas inteligentes*](../secgloss/s-gly.md) conocidos, llame a [**ListCards**](iscarddatabase-listcards.md) o [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6189b-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="6189b-128">Para recuperar el [*proveedor de servicios principal*](../secgloss/p-gly.md) o las interfaces de una tarjeta específica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6189b-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="6189b-129">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="6189b-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="6189b-130">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6189b-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6189b-131">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6189b-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6189b-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6189b-132">Examples</span></span>

<span data-ttu-id="6189b-133">En el ejemplo siguiente se muestra cómo recuperar los nombres de los lectores de tarjetas inteligentes registrados en la base de datos de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="6189b-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="6189b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6189b-134">Requirements</span></span>



| <span data-ttu-id="6189b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6189b-135">Requirement</span></span> | <span data-ttu-id="6189b-136">Value</span><span class="sxs-lookup"><span data-stu-id="6189b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6189b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6189b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6189b-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6189b-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6189b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6189b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6189b-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6189b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6189b-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6189b-141">End of client support</span></span><br/>    | <span data-ttu-id="6189b-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6189b-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6189b-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6189b-143">End of server support</span></span><br/>    | <span data-ttu-id="6189b-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6189b-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6189b-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6189b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6189b-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6189b-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6189b-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="6189b-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6189b-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6189b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6189b-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6189b-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6189b-151">IID</span><span class="sxs-lookup"><span data-stu-id="6189b-151">IID</span></span><br/>                      | <span data-ttu-id="6189b-152">IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6189b-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6189b-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="6189b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6189b-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="6189b-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="6189b-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="6189b-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="6189b-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="6189b-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="6189b-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="6189b-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="6189b-158">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="6189b-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
