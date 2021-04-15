---
description: Devolución de llamada que notifica al host la información de instructrion devuelta por la solicitud asociada.
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderCallback:: ResultInstructions (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63dfd0e3b2b4ec7bd765e5fc0c85835f2a3ce102
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495215"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span data-ttu-id="98d42-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback:: ResultInstructions (método)</span><span class="sxs-lookup"><span data-stu-id="98d42-103"><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>IDebugShaderCallback::ResultInstructions method</span></span>

<span data-ttu-id="98d42-104">Devolución de llamada que notifica al host la información de instructrion devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="98d42-104">A callback that notifies the host of instructrion information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98d42-105">Syntax</span></span>


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a><span data-ttu-id="98d42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98d42-106">Parameters</span></span>

<span data-ttu-id="98d42-107">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="98d42-107">*instructionStreamSize* </span></span>  
<span data-ttu-id="98d42-108">El número de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="98d42-108">The number of instructions.</span></span>

<span data-ttu-id="98d42-109">*count0 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="98d42-109">*count0\_instructionStream* </span></span>  
<span data-ttu-id="98d42-110">Las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="98d42-110">The instructions.</span></span>

## <a name="return-value"></a><span data-ttu-id="98d42-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98d42-111">Return value</span></span>

<span data-ttu-id="98d42-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="98d42-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98d42-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98d42-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d42-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d42-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="98d42-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98d42-115">Header</span></span></p></td><td><span data-ttu-id="98d42-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="98d42-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="98d42-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="98d42-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="98d42-118">**IDebugShaderCallback**</span><span class="sxs-lookup"><span data-stu-id="98d42-118">**IDebugShaderCallback**</span></span>](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
