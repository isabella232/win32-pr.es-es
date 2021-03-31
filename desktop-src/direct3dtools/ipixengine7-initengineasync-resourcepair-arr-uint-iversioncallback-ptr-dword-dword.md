---
description: Pasa los recursos al motor de forma asincrónica, como cadenas para los mensajes de error.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7:: InitEngineAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495725"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="59aac-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7:: InitEngineAsync (método)</span><span class="sxs-lookup"><span data-stu-id="59aac-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="59aac-104">Pasa los recursos al motor de forma asincrónica, como cadenas para los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="59aac-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="59aac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59aac-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="59aac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59aac-106">Parameters</span></span>

<span data-ttu-id="59aac-107">*recursos de count1 \_* </span><span class="sxs-lookup"><span data-stu-id="59aac-107">*count1\_resources* </span></span>  
<span data-ttu-id="59aac-108">Matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="59aac-108">An array of resources.</span></span>

<span data-ttu-id="59aac-109">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="59aac-109">*count* </span></span>  
<span data-ttu-id="59aac-110">El número de recursos de \_ los recursos de count1</span><span class="sxs-lookup"><span data-stu-id="59aac-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="59aac-111">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="59aac-111">*versionCallback* </span></span>  
<span data-ttu-id="59aac-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="59aac-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="59aac-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="59aac-113">*requestCookie* </span></span>  
<span data-ttu-id="59aac-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="59aac-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="59aac-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="59aac-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="59aac-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="59aac-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="59aac-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59aac-117">Return value</span></span>

<span data-ttu-id="59aac-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="59aac-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59aac-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59aac-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59aac-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59aac-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="59aac-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59aac-121">Header</span></span></p></td><td><span data-ttu-id="59aac-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="59aac-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="59aac-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="59aac-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="59aac-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="59aac-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
