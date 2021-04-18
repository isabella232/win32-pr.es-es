---
description: El método GetSubpictureLanguage recupera el idioma de la secuencia de subimagen especificada.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Método GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677043"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="89253-103">Método GetSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="89253-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="89253-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89253-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="89253-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="89253-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="89253-106">El `GetSubpictureLanguage` método recupera el idioma de la secuencia de subimagen especificada.</span><span class="sxs-lookup"><span data-stu-id="89253-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="89253-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89253-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89253-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="89253-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="89253-109">Especifica el número de secuencia de la subimagen cuyo idioma de texto desea recuperar como entero.</span><span class="sxs-lookup"><span data-stu-id="89253-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89253-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89253-110">Return Value</span></span>

<span data-ttu-id="89253-111">Devuelve una cadena legible para el usuario que identifica el idioma de la secuencia de audio en el título actual.</span><span class="sxs-lookup"><span data-stu-id="89253-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



