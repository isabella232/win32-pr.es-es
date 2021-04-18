---
title: CdromCollection. Item (método)
description: El método Item recupera el objeto CDROM en el índice especificado.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase CdromCollection
- Clase CdromCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700310"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="fd8ea-106">CdromCollection. Item (método)</span><span class="sxs-lookup"><span data-stu-id="fd8ea-106">CdromCollection.item method</span></span>

<span data-ttu-id="fd8ea-107">El método **Item** recupera el objeto **CDROM** en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8ea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd8ea-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="fd8ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd8ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8ea-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fd8ea-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ea-111">**Número** (**largo**) que contiene el índice.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8ea-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd8ea-112">Return value</span></span>

<span data-ttu-id="fd8ea-113">Este método devuelve un objeto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="fd8ea-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8ea-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd8ea-114">Remarks</span></span>

<span data-ttu-id="fd8ea-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fd8ea-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fd8ea-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fd8ea-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="fd8ea-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fd8ea-118">Examples</span></span>

<span data-ttu-id="fd8ea-119">En el siguiente ejemplo de JScript se usa *CdromCollection*. **elemento** para imprimir el nombre de la lista de reproducción de cada CD disponible en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="fd8ea-120">Si la unidad contiene realmente contenido de DVD, se requiere Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="fd8ea-121">Se creó un elemento TextArea HTML con el identificador = "listas de reproducción".</span><span class="sxs-lookup"><span data-stu-id="fd8ea-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="fd8ea-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fd8ea-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="fd8ea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd8ea-123">Requirements</span></span>



| <span data-ttu-id="fd8ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd8ea-124">Requirement</span></span> | <span data-ttu-id="fd8ea-125">Value</span><span class="sxs-lookup"><span data-stu-id="fd8ea-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8ea-126">Versión</span><span class="sxs-lookup"><span data-stu-id="fd8ea-126">Version</span></span><br/> | <span data-ttu-id="fd8ea-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fd8ea-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fd8ea-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd8ea-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd8ea-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd8ea-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8ea-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd8ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8ea-131">**CDROM. driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="fd8ea-132">**Objeto CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fd8ea-133">**CdromCollection. Count**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="fd8ea-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="fd8ea-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fd8ea-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fd8ea-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





