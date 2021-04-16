---
description: La propiedad DVDAdm. DefaultAudioLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propiedad DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677175"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="eb425-103">Propiedad DefaultAudioLCID</span><span class="sxs-lookup"><span data-stu-id="eb425-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="eb425-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eb425-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eb425-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="eb425-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eb425-106">La `DVDAdm.DefaultAudioLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="eb425-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="eb425-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb425-107">Return Value</span></span>

<span data-ttu-id="eb425-108">Devuelve un valor entero que representa el LCID de audio predeterminado especificado por el usuario, tal como se almacena en la configuración del registro de la aplicación de DVD.</span><span class="sxs-lookup"><span data-stu-id="eb425-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="eb425-109">Este valor no es necesariamente el mismo que el flujo de audio predeterminado que se creó en el DVD.</span><span class="sxs-lookup"><span data-stu-id="eb425-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb425-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb425-110">Remarks</span></span>

<span data-ttu-id="eb425-111">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eb425-111">This property is read/write with no default value.</span></span> <span data-ttu-id="eb425-112">Si no se especifica ningún LCID de audio predeterminado, el objeto MSDVDAdm reproducirá la secuencia de audio marcada como la secuencia predeterminada en el disco.</span><span class="sxs-lookup"><span data-stu-id="eb425-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb425-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb425-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb425-114">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="eb425-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



