---
description: La propiedad CurrentAudioStream establece o recupera el número de la secuencia de audio habilitada.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propiedad CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659273"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="9c4fc-103">Propiedad CurrentAudioStream</span><span class="sxs-lookup"><span data-stu-id="9c4fc-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="9c4fc-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c4fc-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c4fc-106">La `CurrentAudioStream` propiedad establece o recupera el número de la secuencia de audio habilitada.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="9c4fc-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c4fc-107">Return Value</span></span>

<span data-ttu-id="9c4fc-108">Devuelve un valor entero comprendido entre 0 y 7 que indica la secuencia de audio actual.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c4fc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c4fc-109">Remarks</span></span>

<span data-ttu-id="9c4fc-110">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-110">This property is read/write with no default value.</span></span> <span data-ttu-id="9c4fc-111">Antes de intentar establecer una nueva secuencia de audio, llame a [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para comprobar que la secuencia está disponible.</span><span class="sxs-lookup"><span data-stu-id="9c4fc-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c4fc-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c4fc-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c4fc-113">**AudioStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="9c4fc-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



