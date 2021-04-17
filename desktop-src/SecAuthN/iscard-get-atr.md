---
description: Recupera una cadena ATR de la tarjeta inteligente.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Método ISCard:: get_Atr (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652983"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="0d07c-103">ISCard:: get \_ ATR (método)</span><span class="sxs-lookup"><span data-stu-id="0d07c-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="0d07c-104">\[El método **Get \_ ATR** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0d07c-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0d07c-105">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0d07c-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0d07c-106">El método **Get \_ ATR** recupera una [*cadena ATR*](../secgloss/a-gly.md) de la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d07c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d07c-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="0d07c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d07c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d07c-109">*ppAtr* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d07c-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d07c-110">Puntero a un búfer de bytes en forma de una [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) que contendrá la cadena ATR en la devolución.</span><span class="sxs-lookup"><span data-stu-id="0d07c-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d07c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d07c-111">Return value</span></span>

<span data-ttu-id="0d07c-112">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0d07c-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0d07c-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0d07c-113">Return code</span></span>                                                                                   | <span data-ttu-id="0d07c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d07c-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0d07c-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0d07c-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d07c-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="0d07c-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0d07c-118">El parámetro *ppAtr* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d07c-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="0d07c-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0d07c-120">Se pasó un puntero no válido en *ppAtr*.</span><span class="sxs-lookup"><span data-stu-id="0d07c-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="0d07c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d07c-122">La memoria para satisfacer la solicitud no está disponible.</span><span class="sxs-lookup"><span data-stu-id="0d07c-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d07c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d07c-123">Remarks</span></span>

<span data-ttu-id="0d07c-124">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d07c-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0d07c-125">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0d07c-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0d07c-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d07c-126">Examples</span></span>

<span data-ttu-id="0d07c-127">En el ejemplo siguiente se muestra cómo recuperar la cadena ATR de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="0d07c-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="0d07c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d07c-128">Requirements</span></span>



| <span data-ttu-id="0d07c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d07c-129">Requirement</span></span> | <span data-ttu-id="0d07c-130">Value</span><span class="sxs-lookup"><span data-stu-id="0d07c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d07c-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d07c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0d07c-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0d07c-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d07c-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d07c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0d07c-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d07c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d07c-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0d07c-135">End of client support</span></span><br/>    | <span data-ttu-id="0d07c-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d07c-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0d07c-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0d07c-137">End of server support</span></span><br/>    | <span data-ttu-id="0d07c-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d07c-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0d07c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d07c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d07c-140"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d07c-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0d07c-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d07c-142"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d07c-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d07c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d07c-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d07c-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d07c-145">IID</span><span class="sxs-lookup"><span data-stu-id="0d07c-145">IID</span></span><br/>                      | <span data-ttu-id="0d07c-146">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0d07c-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0d07c-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d07c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d07c-148">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="0d07c-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="0d07c-149">**obtener \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="0d07c-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="0d07c-150">**obtener \_ Protocolo**</span><span class="sxs-lookup"><span data-stu-id="0d07c-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="0d07c-151">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="0d07c-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="0d07c-152">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="0d07c-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="0d07c-153">**IByteBuffer:: Read**</span><span class="sxs-lookup"><span data-stu-id="0d07c-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
