---
title: Método media. getMarkerName
description: El método getMarkerName recupera el nombre del marcador en el índice especificado.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- método getMarkerName de Windows Media Player
- método getMarkerName Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getMarkerName
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700232"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="6ed15-106">Método media. getMarkerName</span><span class="sxs-lookup"><span data-stu-id="6ed15-106">Media.getMarkerName method</span></span>

<span data-ttu-id="6ed15-107">El método **getMarkerName** recupera el nombre del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="6ed15-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed15-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ed15-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="6ed15-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ed15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed15-110">*markerNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ed15-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ed15-111">**Número** (**largo**) que especifica un índice de marcador.</span><span class="sxs-lookup"><span data-stu-id="6ed15-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed15-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ed15-112">Return value</span></span>

<span data-ttu-id="6ed15-113">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="6ed15-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed15-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ed15-114">Remarks</span></span>

<span data-ttu-id="6ed15-115">Este método devuelve **null** si el marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="6ed15-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="6ed15-116">Algunos elementos multimedia digitales no contienen marcadores.</span><span class="sxs-lookup"><span data-stu-id="6ed15-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="6ed15-117">Use **markerCount** para averiguar el número de marcadores que hay en el clip actual.</span><span class="sxs-lookup"><span data-stu-id="6ed15-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="6ed15-118">Los números de índice de marcador empiezan en 1.</span><span class="sxs-lookup"><span data-stu-id="6ed15-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="6ed15-119">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6ed15-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="6ed15-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6ed15-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6ed15-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ed15-121">Examples</span></span>

<span data-ttu-id="6ed15-122">En el siguiente ejemplo de JScript se utiliza el *medio*. **getMarkerName** para rellenar un elemento TEXTAREA HTML denominado MNAMES con los nombres de los marcadores en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="6ed15-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="6ed15-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6ed15-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="6ed15-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed15-124">Requirements</span></span>



| <span data-ttu-id="6ed15-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed15-125">Requirement</span></span> | <span data-ttu-id="6ed15-126">Value</span><span class="sxs-lookup"><span data-stu-id="6ed15-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed15-127">Versión</span><span class="sxs-lookup"><span data-stu-id="6ed15-127">Version</span></span><br/> | <span data-ttu-id="6ed15-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6ed15-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6ed15-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ed15-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ed15-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ed15-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed15-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ed15-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed15-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="6ed15-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6ed15-133">**Media. getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="6ed15-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="6ed15-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="6ed15-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="6ed15-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6ed15-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6ed15-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6ed15-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





