---
description: Descripción constante de ICONSTRUCTEDLOCALE de configuración regional \_
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105995147"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="c51dc-103">configuración regional \_ ICONSTRUCTEDLOCALE</span><span class="sxs-lookup"><span data-stu-id="c51dc-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="c51dc-104">Identificador que se va a solicitar si la configuración regional es una configuración regional "construida".</span><span class="sxs-lookup"><span data-stu-id="c51dc-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="c51dc-105">No se recomienda el uso de este LCTYPE.</span><span class="sxs-lookup"><span data-stu-id="c51dc-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="c51dc-106">Esto identifica una configuración regional para la que Windows muchos no tienen información completa y tiene que "construir" información en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c51dc-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="c51dc-107">Normalmente, la información proporcionada por LOCALE_ICONSTRUCTEDLOCALE es de uso limitado ya que Windows proporcionará tantos datos como estén disponibles para cada configuración regional.</span><span class="sxs-lookup"><span data-stu-id="c51dc-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="c51dc-108">Por lo tanto, no se recomienda el uso de este LCTYPE.</span><span class="sxs-lookup"><span data-stu-id="c51dc-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="c51dc-109">Value</span><span class="sxs-lookup"><span data-stu-id="c51dc-109">Value</span></span> | <span data-ttu-id="c51dc-110">Significado</span><span class="sxs-lookup"><span data-stu-id="c51dc-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="c51dc-111">0</span><span class="sxs-lookup"><span data-stu-id="c51dc-111">0</span></span>     | <span data-ttu-id="c51dc-112">No construido</span><span class="sxs-lookup"><span data-stu-id="c51dc-112">Not constructed</span></span>         |
| <span data-ttu-id="c51dc-113">1</span><span class="sxs-lookup"><span data-stu-id="c51dc-113">1</span></span>     | <span data-ttu-id="c51dc-114">Es una configuración regional construida</span><span class="sxs-lookup"><span data-stu-id="c51dc-114">Is a constructed locale</span></span> |


<span data-ttu-id="c51dc-115">Un ejemplo sería una solicitud de "de-US" o de alemán en el Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="c51dc-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="c51dc-116">NLS usará los datos de idioma alemán que puede encontrar y los datos de la región Estados Unidos que puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="c51dc-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="c51dc-117">Esto puede no ser perfecto como, por ejemplo, es probable que el sistema no tenga información sobre el nombre de Estados Unidos en alemán.</span><span class="sxs-lookup"><span data-stu-id="c51dc-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="c51dc-118">Sin embargo, si la aplicación o el usuario tienen un contexto "de-US", los datos devueltos son los más disponibles.</span><span class="sxs-lookup"><span data-stu-id="c51dc-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="c51dc-119">Las aplicaciones que usan LOCALE_ICONSTRUCTEDLOCALE para rechazar configuraciones regionales y revertir a una configuración regional diferente suelen acabar con una experiencia peor, como el aterrizaje en la de-DE o en-US en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c51dc-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="c51dc-120">Ninguno de ellos está cerca de la solicitud original del idioma alemán con una región Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="c51dc-120">Neither of those are close to the original request for German language with a United States region.</span></span>

