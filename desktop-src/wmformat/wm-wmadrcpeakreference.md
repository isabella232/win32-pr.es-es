---
title: WM/WMADRCPeakReference
description: El atributo WM/WMADRCPeakReference contiene el nivel de volumen máximo del archivo como codificado. Windows Media Player usa este valor para el control de intervalo dinámico. El códec establece este valor y es de solo lectura.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Formato de Windows Media WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419608"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="44594-106">WM/WMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="44594-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="44594-107">El atributo **WM/WMADRCPeakReference** contiene el nivel de volumen máximo del archivo como codificado.</span><span class="sxs-lookup"><span data-stu-id="44594-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="44594-108">Windows Media Player usa este valor para el control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="44594-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="44594-109">El códec establece este valor y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="44594-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="44594-110">Constante global</span><span class="sxs-lookup"><span data-stu-id="44594-110">Global Constant</span></span>

<span data-ttu-id="44594-111">g \_ wszWMWMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="44594-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="44594-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="44594-112">Data Type</span></span>

<span data-ttu-id="44594-113">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="44594-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="44594-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44594-114">Remarks</span></span>

<span data-ttu-id="44594-115">Windows Media Player usa cuatro atributos para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="44594-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="44594-116">El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="44594-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="44594-117">Los valores medios se establecen en el nivel de volumen medio de la secuencia y los valores máximos se establecen en el nivel de volumen máximo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="44594-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="44594-118">Los valores de referencia son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="44594-118">The reference values are read-only.</span></span> <span data-ttu-id="44594-119">Los valores de destino se establecen mediante Windows Media Player cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.</span><span class="sxs-lookup"><span data-stu-id="44594-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="44594-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="44594-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44594-121">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="44594-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="44594-122">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="44594-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="44594-123">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="44594-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="44594-124">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="44594-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




