---
description: La propiedad CurrentSubpictureStream establece o recupera la secuencia de subimagen actual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propiedad CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538079"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="86fee-103">Propiedad CurrentSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="86fee-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="86fee-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="86fee-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86fee-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="86fee-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86fee-106">La `CurrentSubpictureStream` propiedad establece o recupera la secuencia de subimagen actual.</span><span class="sxs-lookup"><span data-stu-id="86fee-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="86fee-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86fee-107">Return Value</span></span>

<span data-ttu-id="86fee-108">Devuelve un valor entero que representa la secuencia.</span><span class="sxs-lookup"><span data-stu-id="86fee-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fee-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86fee-109">Remarks</span></span>

<span data-ttu-id="86fee-110">Los valores posibles de esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="86fee-110">The possible values of this property are:</span></span>



| <span data-ttu-id="86fee-111">Value</span><span class="sxs-lookup"><span data-stu-id="86fee-111">Value</span></span>   | <span data-ttu-id="86fee-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="86fee-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="86fee-113">de 0 a 31</span><span class="sxs-lookup"><span data-stu-id="86fee-113">0 to 31</span></span> | <span data-ttu-id="86fee-114">Secuencia de subimagen</span><span class="sxs-lookup"><span data-stu-id="86fee-114">The subpicture stream</span></span>    |
| <span data-ttu-id="86fee-115">63</span><span class="sxs-lookup"><span data-stu-id="86fee-115">63</span></span>      | <span data-ttu-id="86fee-116">Secuencia de velocidad de bits baja silenciada</span><span class="sxs-lookup"><span data-stu-id="86fee-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="86fee-117">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="86fee-117">This property is read/write with no default value.</span></span> <span data-ttu-id="86fee-118">Antes de establecer una nueva secuencia de subimagen, llame a [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para comprobar que la secuencia está disponible.</span><span class="sxs-lookup"><span data-stu-id="86fee-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="86fee-119">Al establecer esta propiedad, la propiedad [**subpictureon**](subpictureon-property.md) se cambia a **true**.</span><span class="sxs-lookup"><span data-stu-id="86fee-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="86fee-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="86fee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fee-121">**Subimagen en**</span><span class="sxs-lookup"><span data-stu-id="86fee-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="86fee-122">**SubpictureStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="86fee-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



