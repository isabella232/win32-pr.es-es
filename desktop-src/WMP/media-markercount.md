---
title: Media. markerCount
description: La propiedad markerCount recupera el número de marcadores en el elemento multimedia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media Player Windows Media. markerCount
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699815"
---
# <a name="mediamarkercount"></a><span data-ttu-id="88ea9-104">Media. markerCount</span><span class="sxs-lookup"><span data-stu-id="88ea9-104">Media.markerCount</span></span>

<span data-ttu-id="88ea9-105">La propiedad **markerCount** recupera el número de marcadores en el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="88ea9-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ea9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88ea9-106">Syntax</span></span>

<span data-ttu-id="88ea9-107">*reproductor*. *currentMedia*. **markerCount**</span><span class="sxs-lookup"><span data-stu-id="88ea9-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="88ea9-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="88ea9-108">Possible Values</span></span>

<span data-ttu-id="88ea9-109">Esta propiedad es un **número** de solo lectura (**Long**) que especifica el número de marcadores del archivo.</span><span class="sxs-lookup"><span data-stu-id="88ea9-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ea9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88ea9-110">Remarks</span></span>

<span data-ttu-id="88ea9-111">Esta propiedad devuelve cero si un archivo no tiene ningún marcador o si el elemento multimedia no es igual que el *reproductor*. **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="88ea9-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="88ea9-112">Los números de marcador comienzan en 1.</span><span class="sxs-lookup"><span data-stu-id="88ea9-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="88ea9-113">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88ea9-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="88ea9-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="88ea9-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88ea9-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88ea9-115">Examples</span></span>

<span data-ttu-id="88ea9-116">En el siguiente ejemplo de JScript se utiliza el *medio*. **markerCount** para recuperar el número de marcadores en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="88ea9-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="88ea9-117">Ese valor se usa como límite superior para una estructura de bucle, que recorre en iteración la lista de marcadores para recuperar cada nombre de marcador.</span><span class="sxs-lookup"><span data-stu-id="88ea9-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="88ea9-118">Un elemento TEXTAREA HTML denominado MNAMES muestra los nombres de los marcadores en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="88ea9-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="88ea9-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="88ea9-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="88ea9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ea9-120">Requirements</span></span>



| <span data-ttu-id="88ea9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ea9-121">Requirement</span></span> | <span data-ttu-id="88ea9-122">Value</span><span class="sxs-lookup"><span data-stu-id="88ea9-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="88ea9-123">Versión</span><span class="sxs-lookup"><span data-stu-id="88ea9-123">Version</span></span><br/> | <span data-ttu-id="88ea9-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="88ea9-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="88ea9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88ea9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="88ea9-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ea9-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ea9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="88ea9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ea9-128">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="88ea9-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="88ea9-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="88ea9-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="88ea9-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="88ea9-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="88ea9-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="88ea9-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





