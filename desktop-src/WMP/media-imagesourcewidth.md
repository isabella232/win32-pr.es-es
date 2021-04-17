---
title: Media. imageSourceWidth
description: La propiedad imageSourceWidth recupera el ancho del elemento multimedia actual en píxeles.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media Player Windows Media. imageSourceWidth
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699868"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="a7bb6-104">Media. imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="a7bb6-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="a7bb6-105">La propiedad **imageSourceWidth** recupera el ancho del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7bb6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7bb6-106">Syntax</span></span>

<span data-ttu-id="a7bb6-107">*reproductor*. *currentMedia*. **imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="a7bb6-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a7bb6-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a7bb6-108">Possible Values</span></span>

<span data-ttu-id="a7bb6-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a7bb6-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7bb6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7bb6-110">Remarks</span></span>

<span data-ttu-id="a7bb6-111">Si el elemento multimedia no es el actual, esta propiedad devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="a7bb6-112">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="a7bb6-113">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a7bb6-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7bb6-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a7bb6-114">Examples</span></span>

<span data-ttu-id="a7bb6-115">En el siguiente ejemplo de JScript se utiliza el *medio*. **imageSourceWidth** para mostrar el tamaño de la imagen, en píxeles, del **elemento multimedia actual. La información se imprime en un elemento TEXTAREA HTML denominado videosize. El objeto Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a7bb6-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a7bb6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7bb6-116">Requirements</span></span>



| <span data-ttu-id="a7bb6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7bb6-117">Requirement</span></span> | <span data-ttu-id="a7bb6-118">Value</span><span class="sxs-lookup"><span data-stu-id="a7bb6-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7bb6-119">Versión</span><span class="sxs-lookup"><span data-stu-id="a7bb6-119">Version</span></span><br/> | <span data-ttu-id="a7bb6-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a7bb6-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a7bb6-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7bb6-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a7bb6-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7bb6-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7bb6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7bb6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7bb6-124">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="a7bb6-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a7bb6-125">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="a7bb6-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="a7bb6-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a7bb6-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a7bb6-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a7bb6-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





