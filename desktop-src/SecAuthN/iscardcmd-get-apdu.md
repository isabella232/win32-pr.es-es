---
description: Recupera la unidad de datos de protocolo de aplicación (APDU) sin formato.
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Método ISCardCmd:: get_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082140"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="5acea-103">ISCardCmd:: get \_ APDU (método)</span><span class="sxs-lookup"><span data-stu-id="5acea-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="5acea-104">\[El método **Get \_ APDU** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5acea-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5acea-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5acea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5acea-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5acea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5acea-107">El método **Get \_ APDU** recupera la unidad de [*datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) sin procesar.</span><span class="sxs-lookup"><span data-stu-id="5acea-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="5acea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5acea-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="5acea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5acea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5acea-110">*ppApdu* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5acea-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5acea-111">Puntero al búfer de bytes asignado a través de un objeto **IStream** que contiene el mensaje APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="5acea-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5acea-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5acea-112">Return value</span></span>

<span data-ttu-id="5acea-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5acea-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5acea-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5acea-114">Return code</span></span>                                                                                   | <span data-ttu-id="5acea-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5acea-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5acea-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5acea-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5acea-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="5acea-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5acea-119">El parámetro *ppApdu* no es válido.</span><span class="sxs-lookup"><span data-stu-id="5acea-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="5acea-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5acea-121">Se pasó un puntero no válido en *ppApdu*.</span><span class="sxs-lookup"><span data-stu-id="5acea-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="5acea-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5acea-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="5acea-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="5acea-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5acea-124">Remarks</span></span>

<span data-ttu-id="5acea-125">Para copiar las APDU de un objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) en las APDU ajustadas en este objeto de interfaz, llame a [**Put \_ APDU**](iscardcmd-put-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="5acea-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="5acea-126">Para determinar la longitud de las APDU, llame a [**Get \_ ApduLength**](iscardcmd-get-apdulength.md).</span><span class="sxs-lookup"><span data-stu-id="5acea-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="5acea-127">Para obtener una lista de todos los métodos proporcionados por la interfaz [**ISCardCmd**](iscardcmd.md) , vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="5acea-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="5acea-128">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5acea-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5acea-129">Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5acea-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5acea-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5acea-130">Examples</span></span>

<span data-ttu-id="5acea-131">En el ejemplo siguiente se muestra cómo recuperar la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) sin formato (APDU).</span><span class="sxs-lookup"><span data-stu-id="5acea-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="5acea-132">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteApdu es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5acea-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5acea-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5acea-133">Requirements</span></span>



| <span data-ttu-id="5acea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5acea-134">Requirement</span></span> | <span data-ttu-id="5acea-135">Value</span><span class="sxs-lookup"><span data-stu-id="5acea-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5acea-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5acea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5acea-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5acea-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5acea-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5acea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5acea-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5acea-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5acea-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5acea-140">End of client support</span></span><br/>    | <span data-ttu-id="5acea-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5acea-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5acea-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5acea-142">End of server support</span></span><br/>    | <span data-ttu-id="5acea-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5acea-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5acea-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5acea-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5acea-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5acea-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5acea-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="5acea-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5acea-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5acea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5acea-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5acea-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5acea-150">IID</span><span class="sxs-lookup"><span data-stu-id="5acea-150">IID</span></span><br/>                      | <span data-ttu-id="5acea-151">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5acea-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5acea-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5acea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acea-153">**obtener \_ ApduLength**</span><span class="sxs-lookup"><span data-stu-id="5acea-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="5acea-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="5acea-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="5acea-155">**poner \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="5acea-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
