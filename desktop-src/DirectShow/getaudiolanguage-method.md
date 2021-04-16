---
description: El método GetAudioLanguage recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Método GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536639"
---
# <a name="getaudiolanguage-method"></a><span data-ttu-id="3cc36-103">Método GetAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="3cc36-103">GetAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="3cc36-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3cc36-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3cc36-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="3cc36-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3cc36-106">El `GetAudioLanguage` método recupera una cadena que indica qué idioma está disponible en la secuencia de audio especificada.</span><span class="sxs-lookup"><span data-stu-id="3cc36-106">The `GetAudioLanguage` method retrieves a string indicating which language is available on the specified audio stream.</span></span>

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="3cc36-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cc36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc36-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="3cc36-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="3cc36-109">Especifica el número de secuencia de audio del título actual como un entero.</span><span class="sxs-lookup"><span data-stu-id="3cc36-109">Specifies the audio stream number in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc36-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cc36-110">Return Value</span></span>

<span data-ttu-id="3cc36-111">Devuelve una cadena legible para el usuario que identifica el idioma de la secuencia de audio en el título actual.</span><span class="sxs-lookup"><span data-stu-id="3cc36-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



