---
description: El método IsSubpictureStreamEnabled recupera un valor que indica si la secuencia de subimagen especificada está habilitada en el título actual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906778"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="9e661-103">Método IsSubpictureStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="9e661-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="9e661-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9e661-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9e661-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9e661-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9e661-106">El `IsSubpictureStreamEnabled` método recupera un valor que indica si la secuencia de subimagen especificada está habilitada en el título actual.</span><span class="sxs-lookup"><span data-stu-id="9e661-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="9e661-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e661-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e661-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="9e661-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="9e661-109">Especifica el flujo de la subimagen como un entero.</span><span class="sxs-lookup"><span data-stu-id="9e661-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="9e661-110">Value</span><span class="sxs-lookup"><span data-stu-id="9e661-110">Value</span></span>   | <span data-ttu-id="9e661-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e661-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="9e661-112">de 0 a 31</span><span class="sxs-lookup"><span data-stu-id="9e661-112">0 to 31</span></span> | <span data-ttu-id="9e661-113">secuencia de subimagen</span><span class="sxs-lookup"><span data-stu-id="9e661-113">subpicture stream</span></span>        |
| <span data-ttu-id="9e661-114">63</span><span class="sxs-lookup"><span data-stu-id="9e661-114">63</span></span>      | <span data-ttu-id="9e661-115">secuencia de velocidad de bits baja silenciada</span><span class="sxs-lookup"><span data-stu-id="9e661-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e661-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e661-116">Return Value</span></span>

<span data-ttu-id="9e661-117">Devuelve un valor booleano que indica si la secuencia de audio especificada está disponible en el título actual.</span><span class="sxs-lookup"><span data-stu-id="9e661-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="9e661-118">True significa que está disponible.</span><span class="sxs-lookup"><span data-stu-id="9e661-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e661-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e661-119">Remarks</span></span>

<span data-ttu-id="9e661-120">Aunque un disco puede contener hasta 32 secuencias de subimágenes, cada flujo no está necesariamente disponible para cada título.</span><span class="sxs-lookup"><span data-stu-id="9e661-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="9e661-121">Compruebe siempre que haya un flujo disponible para un título antes de establecer la propiedad [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9e661-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



