---
description: Tablas de frecuencia
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tablas de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152016"
---
# <a name="frequency-tables"></a><span data-ttu-id="01635-103">Tablas de frecuencia</span><span class="sxs-lookup"><span data-stu-id="01635-103">Frequency Tables</span></span>

<span data-ttu-id="01635-104">El filtro de sintonizador de TV (kstvtune.ax) tiene una lista interna de tablas de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="01635-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="01635-105">Cada tabla de frecuencias contiene una lista de frecuencias y corresponde a las frecuencias de difusión o de cable para un país o región determinados.</span><span class="sxs-lookup"><span data-stu-id="01635-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="01635-106">Una aplicación se ajusta a una frecuencia determinada llamando al método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con el índice de la frecuencia deseada.</span><span class="sxs-lookup"><span data-stu-id="01635-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="01635-107">En algunos países o regiones, los números de índice de las tablas de frecuencia se asignan directamente a los números de canal.</span><span class="sxs-lookup"><span data-stu-id="01635-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="01635-108">Sin embargo, los números de canal fijos no son adecuados para todos los mercados.</span><span class="sxs-lookup"><span data-stu-id="01635-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="01635-109">Por ejemplo, los consumidores no utilizan realmente los números de canal europeos.</span><span class="sxs-lookup"><span data-stu-id="01635-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="01635-110">En su lugar, los consumidores esperan elegir y asignar sus propios números de canal para las frecuencias que usan los operadores de difusión o cable en su área.</span><span class="sxs-lookup"><span data-stu-id="01635-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="01635-111">En estos países o regiones, las aplicaciones no deben exponer los números de índice directamente al usuario.</span><span class="sxs-lookup"><span data-stu-id="01635-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="01635-112">Instread, la aplicación debe mantener una asignación interna entre los números de canal (presentados al usuario) y los índices de frecuencia (para la optimización).</span><span class="sxs-lookup"><span data-stu-id="01635-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="01635-113">La mayoría de los operadores de cable que no son de Estados Unidos son gratis para difundir las frecuencias de su elección, a menudo mezclando frecuencias de diferentes estándares en la misma línea de canal.</span><span class="sxs-lookup"><span data-stu-id="01635-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="01635-114">Por lo tanto, se usa una tabla de frecuencias de "Unicable" para cualquier país o región que carezca de una entidad de estándares de canal de cable estándar.</span><span class="sxs-lookup"><span data-stu-id="01635-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="01635-115">Además, se proporciona un mecanismo para invalidar las frecuencias individuales en las tablas de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="01635-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="01635-116">Este mecanismo se describe en la sección siguiente, [invalidaciones de frecuencia](frequency-overrides.md).</span><span class="sxs-lookup"><span data-stu-id="01635-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01635-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01635-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01635-118">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="01635-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



