---
description: La propiedad de saldo establece o recupera el equilibrio del altavoz para la salida de la secuencia de audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propiedad balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686408"
---
# <a name="balance-property"></a><span data-ttu-id="f0f14-103">Propiedad balance</span><span class="sxs-lookup"><span data-stu-id="f0f14-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="f0f14-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f0f14-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f0f14-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f0f14-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f0f14-106">La `Balance` propiedad establece o recupera el equilibrio del altavoz para la salida de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="f0f14-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="f0f14-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0f14-107">Return Value</span></span>

<span data-ttu-id="f0f14-108">Devuelve un valor entero que representa los niveles de saldo.</span><span class="sxs-lookup"><span data-stu-id="f0f14-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="f0f14-109">El intervalo de entrada permitido es de-10.000 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="f0f14-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="f0f14-110">Un valor de 0 establece un equilibrio neutro, es decir, los altavoces izquierdo y derecho reciben la misma señal de audio de amplitud.</span><span class="sxs-lookup"><span data-stu-id="f0f14-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f14-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0f14-111">Remarks</span></span>

<span data-ttu-id="f0f14-112">Esta propiedad es de lectura/escritura con un valor predeterminado de 0, lo que significa que ambos altavoces reciben señales de audio equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f0f14-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="f0f14-113">Al igual que con la propiedad de [**volumen**](volume-property.md) , las unidades corresponden a .01 decibelios (multiplicado por-1 cuando</span><span class="sxs-lookup"><span data-stu-id="f0f14-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="f0f14-114">es un valor positivo).</span><span class="sxs-lookup"><span data-stu-id="f0f14-114">is a positive value).</span></span> <span data-ttu-id="f0f14-115">Por ejemplo, un valor de 1000 indica 10 dB en el canal derecho y 90 dB en el canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="f0f14-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



