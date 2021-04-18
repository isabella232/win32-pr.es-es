---
description: Si un evento está disponible, el método NextEvent del objeto SWbemEventSource recupera el evento de una consulta de evento.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource. NextEvent (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707267"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="81a0c-103">SWbemEventSource. NextEvent, método</span><span class="sxs-lookup"><span data-stu-id="81a0c-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="81a0c-104">Si un evento está disponible, el método **NextEvent** del objeto [**SWbemEventSource**](swbemeventsource.md) recupera el evento de una consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="81a0c-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="81a0c-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="81a0c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81a0c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81a0c-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="81a0c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81a0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a0c-108">*iTimeoutMs* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="81a0c-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81a0c-109">Número de milisegundos que la llamada espera un evento antes de devolver un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="81a0c-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="81a0c-110">El valor predeterminado de este parámetro es **wbemTimeoutInfinite** (-1), que dirige la llamada para esperar indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="81a0c-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a0c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81a0c-111">Return value</span></span>

<span data-ttu-id="81a0c-112">Si el método **NextEvent** se ejecuta correctamente, devuelve un objeto [**SWbemObject**](swbemobject.md) que contiene el evento solicitado.</span><span class="sxs-lookup"><span data-stu-id="81a0c-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="81a0c-113">Si se agota el tiempo de espera de la llamada, el objeto devuelto es **null** y se produce un error.</span><span class="sxs-lookup"><span data-stu-id="81a0c-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81a0c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="81a0c-114">Error codes</span></span>

<span data-ttu-id="81a0c-115">Una vez finalizado el método **NextEvent** , el objeto **Err** puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="81a0c-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="81a0c-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="81a0c-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="81a0c-117">El evento solicitado no llegó en la cantidad de tiempo especificada en *iTimeoutMs.*</span><span class="sxs-lookup"><span data-stu-id="81a0c-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81a0c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a0c-118">Requirements</span></span>



| <span data-ttu-id="81a0c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a0c-119">Requirement</span></span> | <span data-ttu-id="81a0c-120">Value</span><span class="sxs-lookup"><span data-stu-id="81a0c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81a0c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="81a0c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81a0c-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81a0c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="81a0c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81a0c-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81a0c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81a0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a0c-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a0c-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81a0c-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="81a0c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="81a0c-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81a0c-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81a0c-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81a0c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a0c-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a0c-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="81a0c-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="81a0c-131">CLSID</span></span><br/>                    | <span data-ttu-id="81a0c-132">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="81a0c-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="81a0c-133">IID</span><span class="sxs-lookup"><span data-stu-id="81a0c-133">IID</span></span><br/>                      | <span data-ttu-id="81a0c-134">\_ISWBEMEVENTSOURCE IID</span><span class="sxs-lookup"><span data-stu-id="81a0c-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




