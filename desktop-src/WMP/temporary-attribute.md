---
title: Atributo temporal
description: El atributo Temporary especifica si una lista de reproducción es temporal.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Media Player de atributos temporales de Windows
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718679"
---
# <a name="temporary-attribute"></a><span data-ttu-id="783ab-104">Atributo temporal</span><span class="sxs-lookup"><span data-stu-id="783ab-104">Temporary Attribute</span></span>

<span data-ttu-id="783ab-105">El atributo **Temporary** especifica si una lista de reproducción es temporal.</span><span class="sxs-lookup"><span data-stu-id="783ab-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="783ab-106">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="783ab-106">**Remarks**</span></span>

<span data-ttu-id="783ab-107">Si recuperó una lista de reproducción de la biblioteca, los cambios que realice en la lista de reproducción se reflejarán en la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="783ab-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="783ab-108">Para evitar esto, llame a [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) pasando el nombre de atributo "Temporary" y el valor "true".</span><span class="sxs-lookup"><span data-stu-id="783ab-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="783ab-109">Esto convierte la instancia de la lista de reproducción en una lista de reproducción temporal, que es segura de editar sin cambiar la lista de reproducción original.</span><span class="sxs-lookup"><span data-stu-id="783ab-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="783ab-110">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="783ab-110">**Applies To**</span></span>

-   [<span data-ttu-id="783ab-111">Reproducción</span><span class="sxs-lookup"><span data-stu-id="783ab-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="783ab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="783ab-112">Requirements</span></span>



| <span data-ttu-id="783ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="783ab-113">Requirement</span></span> | <span data-ttu-id="783ab-114">Value</span><span class="sxs-lookup"><span data-stu-id="783ab-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="783ab-115">Versión</span><span class="sxs-lookup"><span data-stu-id="783ab-115">Version</span></span><br/> | <span data-ttu-id="783ab-116">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="783ab-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="783ab-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="783ab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783ab-118">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="783ab-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





