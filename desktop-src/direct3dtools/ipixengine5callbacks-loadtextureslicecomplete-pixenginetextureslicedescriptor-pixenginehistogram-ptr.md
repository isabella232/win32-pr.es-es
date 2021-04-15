---
description: Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: LoadTextureSliceComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495550"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="f7991-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks:: LoadTextureSliceComplete (método)</span><span class="sxs-lookup"><span data-stu-id="f7991-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="f7991-104">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.</span><span class="sxs-lookup"><span data-stu-id="f7991-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7991-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7991-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="f7991-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7991-106">Parameters</span></span>

<span data-ttu-id="f7991-107">*sliceDesc* </span><span class="sxs-lookup"><span data-stu-id="f7991-107">*sliceDesc* </span></span>  
<span data-ttu-id="f7991-108">Descriptor del segmento cargado.</span><span class="sxs-lookup"><span data-stu-id="f7991-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="f7991-109">*cargas* </span><span class="sxs-lookup"><span data-stu-id="f7991-109">*histogram* </span></span>  
<span data-ttu-id="f7991-110">Dirección de los datos del histograma para el segmento cargado.</span><span class="sxs-lookup"><span data-stu-id="f7991-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7991-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7991-111">Return value</span></span>

<span data-ttu-id="f7991-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f7991-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7991-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7991-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7991-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7991-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f7991-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7991-115">Header</span></span></p></td><td><span data-ttu-id="f7991-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f7991-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f7991-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="f7991-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f7991-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="f7991-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
