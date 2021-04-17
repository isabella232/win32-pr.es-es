---
description: Invalidaciones de frecuencia
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Invalidaciones de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536646"
---
# <a name="frequency-overrides"></a><span data-ttu-id="50f2f-103">Invalidaciones de frecuencia</span><span class="sxs-lookup"><span data-stu-id="50f2f-103">Frequency Overrides</span></span>

<span data-ttu-id="50f2f-104">Se dedicó una cantidad significativa de esfuerzo para asegurarse de que las frecuencias de difusión y las asignaciones estándar de color son correctas para cada país o región.</span><span class="sxs-lookup"><span data-stu-id="50f2f-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="50f2f-105">Incluso, habrá situaciones en las que las tablas de frecuencia no sean suficientes, contengan errores o queden obsoletas.</span><span class="sxs-lookup"><span data-stu-id="50f2f-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="50f2f-106">Para solucionar este problema, las frecuencias enumeradas en las tablas de frecuencia del filtro de sintonizador de TV se pueden invalidar selectivamente, mediante el uso de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="50f2f-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="50f2f-107">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="50f2f-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="50f2f-108">A partir de Windows 7, se usa la siguiente clave del registro redirigida para aplicaciones x86 que se ejecutan en versiones x64 de Windows:</span><span class="sxs-lookup"><span data-stu-id="50f2f-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="50f2f-109">**HKEY \_ Software de \_ equipo local** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="50f2f-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="50f2f-110">Las invalidaciones de frecuencia se agrupan en "espacios de optimización" definidos por la aplicación, que se identifican por número.</span><span class="sxs-lookup"><span data-stu-id="50f2f-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="50f2f-111">En el ejemplo siguiente se muestra una invalidación de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="50f2f-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="50f2f-112">En este caso, "TS0-1" indica el espacio de optimización 0 para las frecuencias de cable.</span><span class="sxs-lookup"><span data-stu-id="50f2f-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="50f2f-113">El primer número identifica el espacio de optimización.</span><span class="sxs-lookup"><span data-stu-id="50f2f-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="50f2f-114">El segundo número es 0 para frecuencias de difusión o 1 para frecuencias de cable.</span><span class="sxs-lookup"><span data-stu-id="50f2f-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="50f2f-115">La subclave denominada "12" invalida el valor de frecuencia de la frecuencia en el índice 12 de la tabla de frecuencias actual.</span><span class="sxs-lookup"><span data-stu-id="50f2f-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="50f2f-116">El valor de la subclave es un valor **DWORD** que especifica la frecuencia en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="50f2f-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="50f2f-117">En este ejemplo, la frecuencia se establece en 67,25 MHz.</span><span class="sxs-lookup"><span data-stu-id="50f2f-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="50f2f-118">Se pueden definir invalidaciones para cualquier número de canal en el intervalo de 1 a 999, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="50f2f-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="50f2f-119">Si el hardware de ajuste no es compatible con una frecuencia determinada, se producirá un error en la solicitud de optimización.</span><span class="sxs-lookup"><span data-stu-id="50f2f-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="50f2f-120">Este mecanismo también puede usarse para crear nuevos números de canal fuera del intervalo existente en la tabla de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="50f2f-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="50f2f-121">El método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devolverá el intervalo de canal extendido.</span><span class="sxs-lookup"><span data-stu-id="50f2f-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="50f2f-122">Por ejemplo, si el intervalo de canales original era de 1 a 158 y se agrega una invalidación de canal de "200" al registro, el método **ChannelMinMax** devolverá 200 como el canal máximo.</span><span class="sxs-lookup"><span data-stu-id="50f2f-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="50f2f-123">En este caso, los números de canal en el intervalo de 159 a 199 no tendrán ninguna frecuencia asignada, por lo que se producirá un error en cualquier solicitud de optimización de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="50f2f-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="50f2f-124">El método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permite a la aplicación elegir el conjunto de invalidaciones y la información de ajuste que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="50f2f-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="50f2f-125">Los números de espacio de optimización son arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="50f2f-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="50f2f-126">Es responsabilidad de la aplicación mantener la relación entre el espacio de optimización y la tabla de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="50f2f-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="50f2f-127">El enfoque más sencillo consiste en usar el código de país o región como el número de espacio de la optimización.</span><span class="sxs-lookup"><span data-stu-id="50f2f-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="50f2f-128">Después, cada vez que la aplicación cambia a un nuevo código de país o región, también cambia al mismo espacio de optimización (en ese orden).</span><span class="sxs-lookup"><span data-stu-id="50f2f-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f2f-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50f2f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f2f-130">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="50f2f-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



