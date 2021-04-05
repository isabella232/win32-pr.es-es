---
description: Establece un nuevo identificador de clase en la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'ISCardCmd: método de ut_ClassId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001386"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="fb08a-103">ISCardCmd::p \_ método de ClassID UT</span><span class="sxs-lookup"><span data-stu-id="fb08a-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="fb08a-104">\[El método **Put \_ ClassID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fb08a-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb08a-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb08a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb08a-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fb08a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fb08a-107">El método **Put \_ ClassID** establece un nuevo identificador de clase en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="fb08a-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb08a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb08a-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="fb08a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb08a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb08a-110">*byClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb08a-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb08a-111">Byte que representa el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="fb08a-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb08a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb08a-112">Return value</span></span>

<span data-ttu-id="fb08a-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="fb08a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fb08a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fb08a-114">Return code</span></span>                                                                                   | <span data-ttu-id="fb08a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb08a-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fb08a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb08a-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb08a-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fb08a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fb08a-119">*ByClass* no es válido.</span><span class="sxs-lookup"><span data-stu-id="fb08a-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="fb08a-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb08a-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="fb08a-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fb08a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb08a-122">Remarks</span></span>

<span data-ttu-id="fb08a-123">Para recuperar el identificador de clase actual, llame a [**Get \_ ClassID**](iscardcmd-get-classid.md).</span><span class="sxs-lookup"><span data-stu-id="fb08a-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="fb08a-124">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="fb08a-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="fb08a-125">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb08a-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fb08a-126">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fb08a-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb08a-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fb08a-127">Examples</span></span>

<span data-ttu-id="fb08a-128">En el ejemplo siguiente se muestra cómo establecer un nuevo identificador de clase en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="fb08a-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="fb08a-129">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="fb08a-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fb08a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb08a-130">Requirements</span></span>



| <span data-ttu-id="fb08a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb08a-131">Requirement</span></span> | <span data-ttu-id="fb08a-132">Value</span><span class="sxs-lookup"><span data-stu-id="fb08a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb08a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb08a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fb08a-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fb08a-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb08a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb08a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fb08a-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb08a-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb08a-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fb08a-137">End of client support</span></span><br/>    | <span data-ttu-id="fb08a-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb08a-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fb08a-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fb08a-139">End of server support</span></span><br/>    | <span data-ttu-id="fb08a-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb08a-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fb08a-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb08a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb08a-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb08a-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fb08a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb08a-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb08a-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb08a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb08a-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb08a-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb08a-147">IID</span><span class="sxs-lookup"><span data-stu-id="fb08a-147">IID</span></span><br/>                      | <span data-ttu-id="fb08a-148">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fb08a-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fb08a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb08a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb08a-150">**obtener \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="fb08a-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="fb08a-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="fb08a-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
