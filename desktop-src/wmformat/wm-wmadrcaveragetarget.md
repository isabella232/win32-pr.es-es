---
title: WM/WMADRCAverageTarget
description: El atributo WM/WMADRCAverageTarget contiene el nivel de volumen medio solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato de Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695514"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="075fa-105">WM/WMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="075fa-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="075fa-106">El atributo **WM/WMADRCAverageTarget** contiene el nivel de volumen medio solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="075fa-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="075fa-107">Windows Media Player usa este valor para el control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="075fa-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="075fa-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="075fa-108">Global Constant</span></span>

<span data-ttu-id="075fa-109">g \_ wszWMWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="075fa-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="075fa-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="075fa-110">Data Type</span></span>

<span data-ttu-id="075fa-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="075fa-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="075fa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="075fa-112">Remarks</span></span>

<span data-ttu-id="075fa-113">Windows Media Player usa cuatro atributos para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="075fa-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="075fa-114">El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="075fa-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="075fa-115">Los valores medios se establecen en el nivel de volumen medio de la secuencia y los valores máximos se establecen en el nivel de volumen máximo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="075fa-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="075fa-116">Los valores de referencia son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="075fa-116">The reference values are read-only.</span></span> <span data-ttu-id="075fa-117">Los valores de destino se establecen mediante Windows Media Player cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.</span><span class="sxs-lookup"><span data-stu-id="075fa-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="075fa-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="075fa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075fa-119">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="075fa-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="075fa-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="075fa-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="075fa-121">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="075fa-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="075fa-122">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="075fa-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




