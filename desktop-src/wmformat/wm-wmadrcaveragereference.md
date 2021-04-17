---
title: WM/WMADRCAverageReference
description: El atributo WM/WMADRCAverageReference contiene el nivel de volumen medio del archivo como codificado.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato de Windows Media WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704859"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="c90c2-104">WM/WMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="c90c2-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="c90c2-105">El atributo **WM/WMADRCAverageReference** contiene el nivel de volumen medio del archivo como codificado.</span><span class="sxs-lookup"><span data-stu-id="c90c2-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c90c2-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="c90c2-106">Global Constant</span></span>

<span data-ttu-id="c90c2-107">g \_ wszWMWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="c90c2-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="c90c2-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c90c2-108">Data Type</span></span>

<span data-ttu-id="c90c2-109">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c90c2-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c90c2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c90c2-110">Remarks</span></span>

<span data-ttu-id="c90c2-111">Windows Media Player usa cuatro atributos para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="c90c2-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="c90c2-112">El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="c90c2-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="c90c2-113">Los valores medios se establecen en el nivel de volumen medio de la secuencia y los valores máximos se establecen en el nivel de volumen máximo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c90c2-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="c90c2-114">Los valores de referencia son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c90c2-114">The reference values are read-only.</span></span> <span data-ttu-id="c90c2-115">Los valores de destino se establecen mediante Windows Media Player cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.</span><span class="sxs-lookup"><span data-stu-id="c90c2-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="c90c2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="c90c2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90c2-117">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="c90c2-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="c90c2-118">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="c90c2-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="c90c2-119">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="c90c2-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="c90c2-120">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="c90c2-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




