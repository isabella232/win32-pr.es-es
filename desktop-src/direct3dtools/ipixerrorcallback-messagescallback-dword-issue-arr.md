---
description: Devolución de llamada que notifica al host de los mensajes devueltos por la solicitud asociada.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixErrorCallback:: MessagesCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105720266"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="4c32e-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback:: MessagesCallback (método)</span><span class="sxs-lookup"><span data-stu-id="4c32e-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="4c32e-104">Devolución de llamada que notifica al host de los mensajes devueltos por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="4c32e-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c32e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c32e-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="4c32e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c32e-106">Parameters</span></span>

<span data-ttu-id="4c32e-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="4c32e-107">*count* </span></span>  
<span data-ttu-id="4c32e-108">El número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4c32e-108">The number of messages.</span></span>

<span data-ttu-id="4c32e-109">*\_mensajes count0* </span><span class="sxs-lookup"><span data-stu-id="4c32e-109">*count0\_messages* </span></span>  
<span data-ttu-id="4c32e-110">Los mensajes.</span><span class="sxs-lookup"><span data-stu-id="4c32e-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c32e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c32e-111">Return value</span></span>

<span data-ttu-id="4c32e-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4c32e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c32e-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c32e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c32e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c32e-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4c32e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c32e-115">Header</span></span></p></td><td><span data-ttu-id="4c32e-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4c32e-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4c32e-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="4c32e-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4c32e-118">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="4c32e-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
