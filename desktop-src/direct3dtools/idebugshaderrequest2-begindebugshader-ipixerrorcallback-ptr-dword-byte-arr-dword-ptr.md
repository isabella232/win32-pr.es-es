---
description: Solicita que inicie la depuración de la lista de instrucciones especificada.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest2:: BeginDebugShader (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152372"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="c33f9-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2:: BeginDebugShader (método)</span><span class="sxs-lookup"><span data-stu-id="c33f9-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="c33f9-104">Solicita que inicie la depuración de la lista de instrucciones especificada.</span><span class="sxs-lookup"><span data-stu-id="c33f9-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c33f9-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="c33f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c33f9-106">Parameters</span></span>

<span data-ttu-id="c33f9-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="c33f9-107">*errorCallback* </span></span>  
<span data-ttu-id="c33f9-108">Dirección de una devolución de llamada para los errores que pueden producirse durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="c33f9-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="c33f9-109">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="c33f9-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="c33f9-110">El número de instrucciones en la secuencia de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="c33f9-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="c33f9-111">*count1 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="c33f9-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="c33f9-112">Secuencia de instrucciones especificada.</span><span class="sxs-lookup"><span data-stu-id="c33f9-112">The specified instruction stream.</span></span>

<span data-ttu-id="c33f9-113">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="c33f9-113">*pDevice* </span></span>  
<span data-ttu-id="c33f9-114">Dirección que se va a pasar al motor de depuración para comunicarse con esta sesión de depuración (motor de depuración readprocessmemory en esta dirección).</span><span class="sxs-lookup"><span data-stu-id="c33f9-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="c33f9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c33f9-115">Return value</span></span>

<span data-ttu-id="c33f9-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c33f9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c33f9-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c33f9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33f9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33f9-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c33f9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c33f9-119">Header</span></span></p></td><td><span data-ttu-id="c33f9-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c33f9-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c33f9-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c33f9-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c33f9-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="c33f9-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
