---
description: El método GetChallenge crea un comando de unidad de datos de protocolo de aplicación (APDU) que emite un desafío (por ejemplo, un número aleatorio) para su uso en un procedimiento relacionado con la seguridad.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'ISCardISO7816:: GetChallenge (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083088"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="89bfc-103">ISCardISO7816:: GetChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="89bfc-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="89bfc-104">\[El método **GetChallenge** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="89bfc-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="89bfc-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89bfc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89bfc-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="89bfc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="89bfc-107">El método **GetChallenge** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que emite un desafío (por ejemplo, un número aleatorio) para su uso en un procedimiento relacionado con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="89bfc-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="89bfc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89bfc-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="89bfc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89bfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89bfc-110">*lBytesExpected* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89bfc-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89bfc-111">Longitud máxima de la respuesta esperada.</span><span class="sxs-lookup"><span data-stu-id="89bfc-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="89bfc-112">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="89bfc-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89bfc-113">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="89bfc-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="89bfc-114">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="89bfc-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="89bfc-115">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="89bfc-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89bfc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89bfc-116">Return value</span></span>

<span data-ttu-id="89bfc-117">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="89bfc-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="89bfc-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="89bfc-118">Return code</span></span>                                                                                   | <span data-ttu-id="89bfc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="89bfc-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="89bfc-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="89bfc-121">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="89bfc-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="89bfc-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="89bfc-123">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="89bfc-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="89bfc-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="89bfc-125">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="89bfc-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="89bfc-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="89bfc-127">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="89bfc-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="89bfc-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89bfc-128">Remarks</span></span>

<span data-ttu-id="89bfc-129">El desafío es válido al menos para el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="89bfc-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="89bfc-130">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="89bfc-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="89bfc-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89bfc-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="89bfc-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="89bfc-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89bfc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89bfc-133">Requirements</span></span>



| <span data-ttu-id="89bfc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="89bfc-134">Requirement</span></span> | <span data-ttu-id="89bfc-135">Value</span><span class="sxs-lookup"><span data-stu-id="89bfc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89bfc-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89bfc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="89bfc-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="89bfc-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89bfc-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89bfc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="89bfc-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89bfc-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89bfc-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="89bfc-140">End of client support</span></span><br/>    | <span data-ttu-id="89bfc-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89bfc-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="89bfc-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="89bfc-142">End of server support</span></span><br/>    | <span data-ttu-id="89bfc-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89bfc-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="89bfc-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89bfc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="89bfc-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="89bfc-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="89bfc-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="89bfc-147"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="89bfc-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89bfc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89bfc-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89bfc-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="89bfc-150">IID</span><span class="sxs-lookup"><span data-stu-id="89bfc-150">IID</span></span><br/>                      | <span data-ttu-id="89bfc-151">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="89bfc-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="89bfc-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="89bfc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89bfc-153">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="89bfc-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="89bfc-154">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="89bfc-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="89bfc-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="89bfc-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
