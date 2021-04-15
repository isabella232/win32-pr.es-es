---
description: Función de devolución de llamada que se usa para notificar al host cuando se ha completado un valor de textura leído.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: ReadTexelValueComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537576"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span data-ttu-id="927ce-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks:: ReadTexelValueComplete (método)</span><span class="sxs-lookup"><span data-stu-id="927ce-103"><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete method</span></span>

<span data-ttu-id="927ce-104">Función de devolución de llamada que se usa para notificar al host cuando se ha completado un valor de textura leído.</span><span class="sxs-lookup"><span data-stu-id="927ce-104">A callback function used to notify the host when a texel value read has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="927ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="927ce-105">Syntax</span></span>


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a><span data-ttu-id="927ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="927ce-106">Parameters</span></span>

<span data-ttu-id="927ce-107">*numChannels* </span><span class="sxs-lookup"><span data-stu-id="927ce-107">*numChannels* </span></span>  
<span data-ttu-id="927ce-108">Número de canales que tiene el textura.</span><span class="sxs-lookup"><span data-stu-id="927ce-108">The number of channels the texel has.</span></span>

<span data-ttu-id="927ce-109">*count0 \_ channelNames* </span><span class="sxs-lookup"><span data-stu-id="927ce-109">*count0\_channelNames* </span></span>  
<span data-ttu-id="927ce-110">Cadenas COM que contienen los nombres de los canales.</span><span class="sxs-lookup"><span data-stu-id="927ce-110">COM strings containing the names of the channels.</span></span>

<span data-ttu-id="927ce-111">*count0 \_ channelValues* </span><span class="sxs-lookup"><span data-stu-id="927ce-111">*count0\_channelValues* </span></span>  
<span data-ttu-id="927ce-112">Valores de los canales.</span><span class="sxs-lookup"><span data-stu-id="927ce-112">The values of the channels.</span></span>

## <a name="return-value"></a><span data-ttu-id="927ce-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="927ce-113">Return value</span></span>

<span data-ttu-id="927ce-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="927ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="927ce-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="927ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="927ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="927ce-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="927ce-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="927ce-117">Header</span></span></p></td><td><span data-ttu-id="927ce-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="927ce-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="927ce-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="927ce-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="927ce-120">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="927ce-120">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
