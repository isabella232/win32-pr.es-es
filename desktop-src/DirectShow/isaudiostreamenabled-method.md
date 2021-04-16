---
description: El método IsAudioStreamEnabled recupera un valor que indica si la secuencia de audio especificada está habilitada en el título actual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536448"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="fcfc1-103">Método IsAudioStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="fcfc1-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="fcfc1-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fcfc1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fcfc1-106">El `IsAudioStreamEnabled` método recupera un valor que indica si la secuencia de audio especificada está habilitada en el título actual.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="fcfc1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcfc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcfc1-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="fcfc1-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="fcfc1-109">Especifica la secuencia de audio como un valor entero comprendido entre 0 y 7.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcfc1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcfc1-110">Return Value</span></span>

<span data-ttu-id="fcfc1-111">Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible para el título actual.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="fcfc1-112">True significa que está disponible.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcfc1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcfc1-113">Remarks</span></span>

<span data-ttu-id="fcfc1-114">Aunque un disco puede contener hasta ocho flujos de audio independientes, cada flujo no está necesariamente disponible para cada título.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="fcfc1-115">Por ejemplo, un título de película principal podría tener tres flujos de audio para inglés, español y japonés, pero el título "próxima atracciones" podría tener solo una secuencia de audio en inglés.</span><span class="sxs-lookup"><span data-stu-id="fcfc1-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="fcfc1-116">Compruebe siempre que haya un flujo disponible para un título antes de establecer la propiedad [**CurrentAudioStream**](currentaudiostream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fcfc1-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



