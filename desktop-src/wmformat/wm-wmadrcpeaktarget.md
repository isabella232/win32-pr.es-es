---
title: WM/WMADRCPeakTarget
description: El atributo WM/WMADRCPeakTarget contiene el nivel de volumen máximo solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Formato de Windows Media WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784145"
---
# <a name="wmwmadrcpeaktarget"></a><span data-ttu-id="b0215-105">WM/WMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="b0215-105">WM/WMADRCPeakTarget</span></span>

<span data-ttu-id="b0215-106">El atributo **WM/WMADRCPeakTarget** contiene el nivel de volumen máximo solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b0215-106">The **WM/WMADRCPeakTarget** attribute contains the maximum volume level requested by the user.</span></span> <span data-ttu-id="b0215-107">Windows Media Player usa este valor para el control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="b0215-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b0215-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="b0215-108">Global Constant</span></span>

<span data-ttu-id="b0215-109">g \_ wszWMWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="b0215-109">g\_wszWMWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="b0215-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b0215-110">Data Type</span></span>

<span data-ttu-id="b0215-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0215-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="b0215-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0215-112">Remarks</span></span>

<span data-ttu-id="b0215-113">Windows Media Player usa cuatro atributos para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="b0215-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="b0215-114">El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="b0215-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="b0215-115">Los valores medios se establecen en el nivel de volumen medio de la secuencia y los valores máximos se establecen en el nivel de volumen máximo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0215-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="b0215-116">Los valores de referencia son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b0215-116">The reference values are read-only.</span></span> <span data-ttu-id="b0215-117">Los valores de destino se establecen mediante Windows Media Player cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.</span><span class="sxs-lookup"><span data-stu-id="b0215-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0215-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0215-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0215-119">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="b0215-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="b0215-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="b0215-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="b0215-121">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="b0215-121">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="b0215-122">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="b0215-122">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




