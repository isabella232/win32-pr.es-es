---
title: Lista de reproducción. attributeCount
description: La propiedad attributeCount recupera el número de atributos asociados a la lista de reproducción.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Windows Media Player de lista de reproducción. attributeCount
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708970"
---
# <a name="playlistattributecount"></a><span data-ttu-id="efcd4-104">Lista de reproducción. attributeCount</span><span class="sxs-lookup"><span data-stu-id="efcd4-104">Playlist.attributeCount</span></span>

<span data-ttu-id="efcd4-105">La propiedad **attributeCount** recupera el número de atributos asociados a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="efcd4-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="efcd4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efcd4-106">Syntax</span></span>

<span data-ttu-id="efcd4-107">*reproductor*. *currentPlaylist*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="efcd4-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="efcd4-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="efcd4-108">Possible Values</span></span>

<span data-ttu-id="efcd4-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="efcd4-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="efcd4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efcd4-110">Remarks</span></span>

<span data-ttu-id="efcd4-111">Dado que las listas de reproducción pueden provienen de muchos orígenes diferentes, pueden tener varios conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="efcd4-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="efcd4-112">Este método recupera el número total de propiedades disponibles para que los demás métodos del objeto de **lista de reproducción** puedan tener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="efcd4-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="efcd4-113">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="efcd4-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="efcd4-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="efcd4-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="efcd4-115">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="efcd4-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="efcd4-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="efcd4-116">Examples</span></span>

<span data-ttu-id="efcd4-117">En el ejemplo de JScript siguiente se muestra cómo se utilizan varias propiedades y métodos de la **lista de reproducción** y los objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="efcd4-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="efcd4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efcd4-118">Requirements</span></span>



| <span data-ttu-id="efcd4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="efcd4-119">Requirement</span></span> | <span data-ttu-id="efcd4-120">Value</span><span class="sxs-lookup"><span data-stu-id="efcd4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="efcd4-121">Versión</span><span class="sxs-lookup"><span data-stu-id="efcd4-121">Version</span></span><br/> | <span data-ttu-id="efcd4-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="efcd4-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="efcd4-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efcd4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="efcd4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efcd4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efcd4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="efcd4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efcd4-126">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="efcd4-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="efcd4-127">**Lista de reproducción. attributeName**</span><span class="sxs-lookup"><span data-stu-id="efcd4-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="efcd4-128">**Lista de reproducción. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="efcd4-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="efcd4-129">**Lista de reproducción. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="efcd4-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="efcd4-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="efcd4-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="efcd4-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="efcd4-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





