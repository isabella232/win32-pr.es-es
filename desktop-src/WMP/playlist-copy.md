---
title: Lista de reproducción. copia
description: El método de copia inicia una operación de copia desde el CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Lista de reproducción. copiar Media Player de Windows
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708864"
---
# <a name="playlistcopy"></a><span data-ttu-id="dcf22-104">Lista de reproducción. copia</span><span class="sxs-lookup"><span data-stu-id="dcf22-104">PLAYLIST.copy</span></span>

<span data-ttu-id="dcf22-105">El método de **copia** inicia una operación de copia desde el CD.</span><span class="sxs-lookup"><span data-stu-id="dcf22-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="dcf22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcf22-106">Parameters</span></span>

<span data-ttu-id="dcf22-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dcf22-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcf22-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcf22-108">Return Value</span></span>

<span data-ttu-id="dcf22-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dcf22-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf22-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcf22-110">Remarks</span></span>

<span data-ttu-id="dcf22-111">Este método solo copia los elementos activados en la lista de reproducción y funciona de la misma manera que en el panel **Copiar desde CD** en el modo completo de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dcf22-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="dcf22-112">Para que este método funcione, debe haber un CD en la unidad de CD.</span><span class="sxs-lookup"><span data-stu-id="dcf22-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="dcf22-113">Establezca el atributo **checkboxesVisible** en true para permitir que los usuarios seleccionen elementos individuales en un CD antes de la copia.</span><span class="sxs-lookup"><span data-stu-id="dcf22-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf22-114">Requirements</span></span>



| <span data-ttu-id="dcf22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf22-115">Requirement</span></span> | <span data-ttu-id="dcf22-116">Value</span><span class="sxs-lookup"><span data-stu-id="dcf22-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dcf22-117">Versión</span><span class="sxs-lookup"><span data-stu-id="dcf22-117">Version</span></span><br/> | <span data-ttu-id="dcf22-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dcf22-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcf22-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcf22-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf22-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="dcf22-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="dcf22-121">**Lista de reproducción. abortCopy**</span><span class="sxs-lookup"><span data-stu-id="dcf22-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="dcf22-122">**Lista de reproducción. copiando**</span><span class="sxs-lookup"><span data-stu-id="dcf22-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





