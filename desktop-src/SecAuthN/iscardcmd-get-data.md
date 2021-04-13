---
description: Recupera el campo de datos de la unidad de datos de protocolo de aplicación (APDU), colocándolo en un objeto de búfer de bytes.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Método ISCardCmd:: get_Data (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546987"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="d4d99-103">ISCardCmd:: get \_ Data (método)</span><span class="sxs-lookup"><span data-stu-id="d4d99-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="d4d99-104">\[El método **obtener \_ datos** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="d4d99-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d4d99-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d4d99-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d4d99-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d4d99-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d4d99-107">El método **Get \_ Data** recupera el campo de datos de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU), colocándolo en un objeto de búfer de bytes.</span><span class="sxs-lookup"><span data-stu-id="d4d99-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d99-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4d99-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d4d99-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4d99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d99-110">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d4d99-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d99-111">Puntero al objeto de búfer de bytes (**IStream**) que contiene el campo de datos APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="d4d99-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d99-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4d99-112">Return value</span></span>

<span data-ttu-id="d4d99-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d4d99-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d4d99-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d4d99-114">Return code</span></span>                                                                                   | <span data-ttu-id="d4d99-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4d99-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d4d99-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d4d99-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4d99-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d4d99-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d4d99-119">El parámetro *ppData* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d4d99-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d4d99-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d4d99-121">Se pasó un puntero no válido en *ppData*.</span><span class="sxs-lookup"><span data-stu-id="d4d99-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="d4d99-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d4d99-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d4d99-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d4d99-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4d99-124">Remarks</span></span>

<span data-ttu-id="d4d99-125">Para establecer el campo de datos de APDU, llame a [**Put \_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="d4d99-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="d4d99-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d4d99-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d4d99-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4d99-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d4d99-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d4d99-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d4d99-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4d99-129">Examples</span></span>

<span data-ttu-id="d4d99-130">En el ejemplo siguiente se muestra cómo recuperar el campo de datos de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="d4d99-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="d4d99-131">En el ejemplo se da por supuesto que pIByteData es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d99-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d4d99-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d99-132">Requirements</span></span>



| <span data-ttu-id="d4d99-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d99-133">Requirement</span></span> | <span data-ttu-id="d4d99-134">Value</span><span class="sxs-lookup"><span data-stu-id="d4d99-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d99-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d99-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d99-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d99-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d4d99-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d99-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d99-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d99-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4d99-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d4d99-139">End of client support</span></span><br/>    | <span data-ttu-id="d4d99-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4d99-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d4d99-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d4d99-141">End of server support</span></span><br/>    | <span data-ttu-id="d4d99-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4d99-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d4d99-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4d99-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d99-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4d99-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d4d99-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4d99-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4d99-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4d99-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d99-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d99-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4d99-149">IID</span><span class="sxs-lookup"><span data-stu-id="d4d99-149">IID</span></span><br/>                      | <span data-ttu-id="d4d99-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d4d99-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d4d99-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4d99-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d99-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d4d99-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="d4d99-153">**colocar \_ datos**</span><span class="sxs-lookup"><span data-stu-id="d4d99-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
