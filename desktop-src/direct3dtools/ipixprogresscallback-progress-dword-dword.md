---
description: Devolución de llamada que notifica al host el progreso de una solicitud asociada.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback::P método rogress
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422928"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="7f854-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::P método rogress</span><span class="sxs-lookup"><span data-stu-id="7f854-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="7f854-104">Devolución de llamada que notifica al host el progreso de una solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="7f854-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f854-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f854-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="7f854-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f854-106">Parameters</span></span>

<span data-ttu-id="7f854-107">*corrientes* </span><span class="sxs-lookup"><span data-stu-id="7f854-107">*current* </span></span>  
<span data-ttu-id="7f854-108">La parte de una solicitud se completó, como un recuento del número de pasos completados.</span><span class="sxs-lookup"><span data-stu-id="7f854-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="7f854-109">*Tamañomáximo* </span><span class="sxs-lookup"><span data-stu-id="7f854-109">*maxSize* </span></span>  
<span data-ttu-id="7f854-110">El número total de pasos para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f854-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f854-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f854-111">Return value</span></span>

<span data-ttu-id="7f854-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7f854-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f854-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f854-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f854-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f854-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7f854-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f854-115">Header</span></span></p></td><td><span data-ttu-id="7f854-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7f854-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7f854-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="7f854-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7f854-118">**IPixProgressCallback**</span><span class="sxs-lookup"><span data-stu-id="7f854-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
