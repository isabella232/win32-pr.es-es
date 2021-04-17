---
title: THEME. playSound
description: El método playSound reproduce el archivo de sonido especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Media Player de Windows THEME. playSound
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690451"
---
# <a name="themeplaysound"></a><span data-ttu-id="6c20d-104">THEME. playSound</span><span class="sxs-lookup"><span data-stu-id="6c20d-104">THEME.playSound</span></span>

<span data-ttu-id="6c20d-105">El método **playSound** reproduce el archivo de sonido especificado.</span><span class="sxs-lookup"><span data-stu-id="6c20d-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="6c20d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c20d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c20d-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="6c20d-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="6c20d-108">**Cadena** que especifica el nombre del archivo de sonido que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="6c20d-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c20d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c20d-109">Return Value</span></span>

<span data-ttu-id="6c20d-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6c20d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c20d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c20d-111">Remarks</span></span>

<span data-ttu-id="6c20d-112">Este método permite agregar efectos de sonido a una máscara, por ejemplo, cuando se hace clic en los botones.</span><span class="sxs-lookup"><span data-stu-id="6c20d-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="6c20d-113">El sistema operativo reproduce el sonido directamente y no lo hace Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6c20d-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="6c20d-114">Esto significa que no se puede controlar el sonido con los métodos y la configuración de Windows Media Player, pero se puede reproducir mientras Windows Media Player está reproduciendo otro archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="6c20d-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="6c20d-115">Este método solo admite archivos WAV.</span><span class="sxs-lookup"><span data-stu-id="6c20d-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c20d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c20d-116">Requirements</span></span>



| <span data-ttu-id="6c20d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c20d-117">Requirement</span></span> | <span data-ttu-id="6c20d-118">Value</span><span class="sxs-lookup"><span data-stu-id="6c20d-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6c20d-119">Versión</span><span class="sxs-lookup"><span data-stu-id="6c20d-119">Version</span></span><br/> | <span data-ttu-id="6c20d-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="6c20d-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c20d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c20d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c20d-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="6c20d-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





