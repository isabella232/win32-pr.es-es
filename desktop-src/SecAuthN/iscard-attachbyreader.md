---
description: El método AttachByReader abre la tarjeta inteligente en el lector con nombre.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'ISCard:: AttachByReader (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002754"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="63878-103">ISCard:: AttachByReader (método)</span><span class="sxs-lookup"><span data-stu-id="63878-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="63878-104">\[El método **AttachByReader** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="63878-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63878-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63878-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63878-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="63878-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="63878-107">El método **AttachByReader** abre la [*tarjeta inteligente*](../secgloss/s-gly.md) en el [*lector*](../secgloss/r-gly.md)con nombre.</span><span class="sxs-lookup"><span data-stu-id="63878-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63878-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63878-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="63878-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63878-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63878-110">*bstrReaderName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63878-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63878-111">**BSTR** que contiene el nombre del lector de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="63878-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="63878-112">*ShareMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63878-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63878-113">Modo en el que se va a notificar el acceso a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="63878-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="63878-114">Value</span><span class="sxs-lookup"><span data-stu-id="63878-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="63878-115">Significado</span><span class="sxs-lookup"><span data-stu-id="63878-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="63878-116"><dt>**ÚNICO**</dt></span><span class="sxs-lookup"><span data-stu-id="63878-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="63878-117">Nadie más usa esta conexión con la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="63878-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="63878-118"><dt>**RECURSO**</dt></span><span class="sxs-lookup"><span data-stu-id="63878-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="63878-119">Otras aplicaciones pueden usar esta conexión.</span><span class="sxs-lookup"><span data-stu-id="63878-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="63878-120">*PrefProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63878-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63878-121">Valor de protocolo preferido.</span><span class="sxs-lookup"><span data-stu-id="63878-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="63878-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="63878-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="63878-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="63878-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="63878-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="63878-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="63878-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="63878-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63878-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63878-126">Return value</span></span>

<span data-ttu-id="63878-127">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="63878-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="63878-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="63878-128">Return code</span></span>                                                                                  | <span data-ttu-id="63878-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="63878-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63878-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="63878-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="63878-131">Abrir en la tarjeta inteligente en el lector con nombre se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="63878-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="63878-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63878-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="63878-133">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="63878-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63878-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63878-134">Remarks</span></span>

<span data-ttu-id="63878-135">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63878-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="63878-136">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="63878-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="63878-137">Cuando haya terminado de usar el lector, libere los datos adjuntos llamando al método [**ISCard::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="63878-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="63878-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="63878-138">Examples</span></span>

<span data-ttu-id="63878-139">En el ejemplo siguiente se muestra cómo conectarse a una tarjeta inteligente en un lector de tarjeta inteligente especificado.</span><span class="sxs-lookup"><span data-stu-id="63878-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="63878-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63878-140">Requirements</span></span>



| <span data-ttu-id="63878-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="63878-141">Requirement</span></span> | <span data-ttu-id="63878-142">Value</span><span class="sxs-lookup"><span data-stu-id="63878-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63878-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63878-143">Minimum supported client</span></span><br/> | <span data-ttu-id="63878-144">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="63878-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63878-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63878-145">Minimum supported server</span></span><br/> | <span data-ttu-id="63878-146">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63878-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63878-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="63878-147">End of client support</span></span><br/>    | <span data-ttu-id="63878-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="63878-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="63878-149">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="63878-149">End of server support</span></span><br/>    | <span data-ttu-id="63878-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63878-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="63878-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63878-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="63878-152"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="63878-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="63878-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="63878-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="63878-154"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63878-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63878-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63878-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63878-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63878-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63878-157">IID</span><span class="sxs-lookup"><span data-stu-id="63878-157">IID</span></span><br/>                      | <span data-ttu-id="63878-158">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="63878-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="63878-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="63878-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63878-160">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="63878-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="63878-161">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="63878-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="63878-162">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="63878-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="63878-163">**Volver a adjuntar**</span><span class="sxs-lookup"><span data-stu-id="63878-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
