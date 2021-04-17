---
title: Método media. getMarkerTime
description: El método getMarkerTime recupera la hora del marcador en el índice especificado.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- método getMarkerTime de Windows Media Player
- método getMarkerTime Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700144"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="68bb5-106">Método media. getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="68bb5-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="68bb5-107">El método **getMarkerTime** recupera la hora del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="68bb5-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bb5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68bb5-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="68bb5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68bb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68bb5-110">*markerNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68bb5-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68bb5-111">**Número** (**largo**) que especifica el índice del marcador.</span><span class="sxs-lookup"><span data-stu-id="68bb5-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68bb5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68bb5-112">Return value</span></span>

<span data-ttu-id="68bb5-113">Este método devuelve un **número** (**Double**) que especifica la ubicación del marcador en segundos desde el principio del clip.</span><span class="sxs-lookup"><span data-stu-id="68bb5-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bb5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68bb5-114">Remarks</span></span>

<span data-ttu-id="68bb5-115">Este método devuelve **null** si el marcador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="68bb5-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="68bb5-116">Algunos elementos multimedia digitales no contienen marcadores.</span><span class="sxs-lookup"><span data-stu-id="68bb5-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="68bb5-117">Use **markerCount** para averiguar el número de marcadores que hay en el clip actual.</span><span class="sxs-lookup"><span data-stu-id="68bb5-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="68bb5-118">Los números de índice de marcador empiezan en 1.</span><span class="sxs-lookup"><span data-stu-id="68bb5-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="68bb5-119">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="68bb5-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="68bb5-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="68bb5-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="68bb5-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68bb5-121">Examples</span></span>

<span data-ttu-id="68bb5-122">En el siguiente ejemplo de JScript se utiliza el *medio*. **getMarkerTime** para rellenar un elemento TEXTAREA HTML denominado MTIMES con la ubicación de cada marcador.</span><span class="sxs-lookup"><span data-stu-id="68bb5-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="68bb5-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="68bb5-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="68bb5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68bb5-124">Requirements</span></span>



| <span data-ttu-id="68bb5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="68bb5-125">Requirement</span></span> | <span data-ttu-id="68bb5-126">Value</span><span class="sxs-lookup"><span data-stu-id="68bb5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68bb5-127">Versión</span><span class="sxs-lookup"><span data-stu-id="68bb5-127">Version</span></span><br/> | <span data-ttu-id="68bb5-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="68bb5-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="68bb5-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68bb5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="68bb5-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68bb5-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bb5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="68bb5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bb5-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="68bb5-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="68bb5-133">**Media. getMarkerName**</span><span class="sxs-lookup"><span data-stu-id="68bb5-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="68bb5-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="68bb5-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="68bb5-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="68bb5-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="68bb5-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="68bb5-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





