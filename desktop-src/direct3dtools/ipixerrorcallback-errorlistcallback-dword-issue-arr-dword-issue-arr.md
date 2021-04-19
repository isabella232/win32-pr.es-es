---
description: Devolución de llamada que notifica al host de errores devueltos por la solicitud asociada.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixErrorCallback:: ErrorListCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105720271"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="66ed1-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback:: ErrorListCallback (método)</span><span class="sxs-lookup"><span data-stu-id="66ed1-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="66ed1-104">Devolución de llamada que notifica al host de errores devueltos por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="66ed1-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ed1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66ed1-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="66ed1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66ed1-106">Parameters</span></span>

<span data-ttu-id="66ed1-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="66ed1-107">*count* </span></span>  
<span data-ttu-id="66ed1-108">Número de errores.</span><span class="sxs-lookup"><span data-stu-id="66ed1-108">The number of errors.</span></span>

<span data-ttu-id="66ed1-109">*count0 \_ errores* </span><span class="sxs-lookup"><span data-stu-id="66ed1-109">*count0\_errorList* </span></span>  
<span data-ttu-id="66ed1-110">Los errores.</span><span class="sxs-lookup"><span data-stu-id="66ed1-110">The errors.</span></span>

<span data-ttu-id="66ed1-111">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="66ed1-111">*count* </span></span>  
<span data-ttu-id="66ed1-112">Número de advertencias.</span><span class="sxs-lookup"><span data-stu-id="66ed1-112">The number of warningns.</span></span>

<span data-ttu-id="66ed1-113">*count0 \_ warningList* </span><span class="sxs-lookup"><span data-stu-id="66ed1-113">*count0\_warningList* </span></span>  
<span data-ttu-id="66ed1-114">Advertencias.</span><span class="sxs-lookup"><span data-stu-id="66ed1-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="66ed1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66ed1-115">Return value</span></span>

<span data-ttu-id="66ed1-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="66ed1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66ed1-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66ed1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ed1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ed1-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="66ed1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66ed1-119">Header</span></span></p></td><td><span data-ttu-id="66ed1-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="66ed1-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="66ed1-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="66ed1-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="66ed1-122">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="66ed1-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
