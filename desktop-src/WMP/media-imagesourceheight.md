---
title: Media. imageSourceHeight
description: La propiedad ImageSourceHeight recupera el alto del elemento multimedia actual en píxeles.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media Player Windows Media. imageSourceHeight
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699869"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="4e7e2-104">Media. imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="4e7e2-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="4e7e2-105">La propiedad **ImageSourceHeight** recupera el alto del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7e2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e7e2-106">Syntax</span></span>

<span data-ttu-id="4e7e2-107">*reproductor*. *currentMedia*. **imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="4e7e2-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4e7e2-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4e7e2-108">Possible Values</span></span>

<span data-ttu-id="4e7e2-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4e7e2-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7e2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e7e2-110">Remarks</span></span>

<span data-ttu-id="4e7e2-111">Si el elemento multimedia no es el actual, esta propiedad devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="4e7e2-112">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="4e7e2-113">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4e7e2-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4e7e2-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e7e2-114">Examples</span></span>

<span data-ttu-id="4e7e2-115">En el siguiente ejemplo de JScript se utiliza *media*. imageSourceHeight para mostrar el tamaño de la imagen, en píxeles, del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="4e7e2-116">La información se imprime en un elemento TEXTAREA HTML denominado videosize.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="4e7e2-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4e7e2-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="4e7e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e7e2-118">Requirements</span></span>



| <span data-ttu-id="4e7e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7e2-119">Requirement</span></span> | <span data-ttu-id="4e7e2-120">Value</span><span class="sxs-lookup"><span data-stu-id="4e7e2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7e2-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4e7e2-121">Version</span></span><br/> | <span data-ttu-id="4e7e2-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4e7e2-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4e7e2-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e7e2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e7e2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e7e2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7e2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e7e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7e2-126">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="4e7e2-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="4e7e2-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="4e7e2-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="4e7e2-128">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="4e7e2-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4e7e2-129">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="4e7e2-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





