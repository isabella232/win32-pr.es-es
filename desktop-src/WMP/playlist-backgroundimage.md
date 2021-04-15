---
title: Lista de reproducción. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Lista de reproducción. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708979"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="2ee63-104">Lista de reproducción. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="2ee63-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="2ee63-105">El atributo **BackgroundImage** especifica o recupera la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="2ee63-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="2ee63-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2ee63-106">Possible Values</span></span>

<span data-ttu-id="2ee63-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="2ee63-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="2ee63-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2ee63-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee63-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ee63-109">Remarks</span></span>

<span data-ttu-id="2ee63-110">Si el alto y el ancho de la imagen son más pequeños que el alto y el ancho del elemento de **lista de reproducción** , la imagen se coloca en mosaico.</span><span class="sxs-lookup"><span data-stu-id="2ee63-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="2ee63-111">Los formatos admitidos son BMP, JPG, GIF y PNG.</span><span class="sxs-lookup"><span data-stu-id="2ee63-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="2ee63-112">Si se especifica un valor de "degradado" para la imagen de fondo, el fondo de la lista de reproducción se mostrará como degradado de color.</span><span class="sxs-lookup"><span data-stu-id="2ee63-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="2ee63-113">Esto significa que el color de fondo pasa gradualmente entre la [lista de reproducción. BackgroundColor](playlist-backgroundcolor.md) (en la parte superior de los fondos) y los valores de [lista de reproducción. statusColor](playlist-statuscolor.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee63-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee63-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee63-114">Requirements</span></span>



| <span data-ttu-id="2ee63-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee63-115">Requirement</span></span> | <span data-ttu-id="2ee63-116">Value</span><span class="sxs-lookup"><span data-stu-id="2ee63-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee63-117">Versión</span><span class="sxs-lookup"><span data-stu-id="2ee63-117">Version</span></span><br/> | <span data-ttu-id="2ee63-118">Windows Media Player versión 7,0 o posterior, Windows Media Player 10 para la característica de degradado</span><span class="sxs-lookup"><span data-stu-id="2ee63-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ee63-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ee63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee63-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2ee63-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





