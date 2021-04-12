---
description: El método CANCEL del objeto SWbemSink cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink:: CANCEL (método) (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279287"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="e27b6-103">ISWbemSink:: CANCEL (método)</span><span class="sxs-lookup"><span data-stu-id="e27b6-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="e27b6-104">El método **Cancel** del objeto [**SWbemSink**](swbemsink.md) cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="e27b6-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="e27b6-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e27b6-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e27b6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e27b6-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="e27b6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e27b6-107">Parameters</span></span>

<span data-ttu-id="e27b6-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e27b6-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e27b6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e27b6-109">Return value</span></span>

<span data-ttu-id="e27b6-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e27b6-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e27b6-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e27b6-111">Error codes</span></span>

<span data-ttu-id="e27b6-112">Después de completar el método **Cancel** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="e27b6-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="e27b6-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e27b6-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e27b6-114">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e27b6-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e27b6-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e27b6-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e27b6-116">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="e27b6-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e27b6-117">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="e27b6-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="e27b6-118">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="e27b6-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="e27b6-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e27b6-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="e27b6-120">El nombre de usuario y la contraseña actuales o especificados no son válidos o están autorizados para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="e27b6-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e27b6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e27b6-121">Remarks</span></span>

<span data-ttu-id="e27b6-122">No se puede cancelar solo una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e27b6-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="e27b6-123">Si hay varias llamadas asincrónicas pendientes que utilizan este receptor de objetos, este método cancela todas las llamadas asincrónicas que utilizan este receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="e27b6-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="e27b6-124">Las llamadas asincrónicas que están asociadas a otros receptores de objeto continúan sin efecto.</span><span class="sxs-lookup"><span data-stu-id="e27b6-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="e27b6-125">No se puede asignar este receptor a **Nothing** para cancelar una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e27b6-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="e27b6-126">Debe llamar al método **Cancel** para que WMI interrumpa la operación y libere los recursos asociados.</span><span class="sxs-lookup"><span data-stu-id="e27b6-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="e27b6-127">Esto es muy importante con operaciones asincrónicas largas, como consultas u operaciones que nunca se completan, como [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="e27b6-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="e27b6-128">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="e27b6-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="e27b6-129">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e27b6-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="e27b6-130">Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="e27b6-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="e27b6-131">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e27b6-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="e27b6-132">En el ejemplo siguiente se muestra cómo cancelar una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e27b6-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="e27b6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e27b6-133">Requirements</span></span>



| <span data-ttu-id="e27b6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e27b6-134">Requirement</span></span> | <span data-ttu-id="e27b6-135">Value</span><span class="sxs-lookup"><span data-stu-id="e27b6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e27b6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e27b6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e27b6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e27b6-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e27b6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e27b6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e27b6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e27b6-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e27b6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e27b6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e27b6-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e27b6-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e27b6-142">IDL</span><span class="sxs-lookup"><span data-stu-id="e27b6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e27b6-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e27b6-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e27b6-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e27b6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e27b6-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e27b6-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e27b6-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="e27b6-146">CLSID</span></span><br/>                    | <span data-ttu-id="e27b6-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="e27b6-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="e27b6-148">IID</span><span class="sxs-lookup"><span data-stu-id="e27b6-148">IID</span></span><br/>                      | <span data-ttu-id="e27b6-149">\_ISWBEMSINK IID</span><span class="sxs-lookup"><span data-stu-id="e27b6-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="e27b6-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="e27b6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27b6-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="e27b6-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

