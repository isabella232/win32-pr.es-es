---
title: IAMWMBufferPass SetNotify, método
description: Las aplicaciones usan el método SetNotify para proporcionar el filtro WM ASF Writer o el lector ASF de WM con un puntero a la interfaz IAMWMBufferPassCallback de la aplicación.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Método SetNotify formato de Windows Media
- Método SetNotify formato de Windows Media, interfaz IAMWMBufferPass
- Interfaz IAMWMBufferPass formato de Windows Media, método SetNotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421247"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="bd3af-106">IAMWMBufferPass:: SetNotify (método)</span><span class="sxs-lookup"><span data-stu-id="bd3af-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="bd3af-107">Las aplicaciones usan el método **SetNotify** para proporcionar el filtro WM ASF Writer o el [lector ASF de WM](wm-asf-reader-filter.md) con un puntero a la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd3af-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3af-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd3af-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="bd3af-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd3af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3af-110">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd3af-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3af-111">Puntero a la interfaz **IAMWMBufferPassCallback** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd3af-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3af-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3af-112">Return value</span></span>

<span data-ttu-id="bd3af-113">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="bd3af-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="bd3af-114">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd3af-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3af-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd3af-115">Remarks</span></span>

<span data-ttu-id="bd3af-116">Llame a este método antes de colocar el gráfico de filtro en el estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="bd3af-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd3af-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd3af-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3af-118">**Interfaz IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="bd3af-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 