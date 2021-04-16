---
title: PlaylistArray. Item (método)
description: El método Item recupera la lista de reproducción en el índice especificado.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase PlaylistArray
- Clase PlaylistArray Windows Media Player, método Item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718890"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="5aa3f-106">PlaylistArray. Item (método)</span><span class="sxs-lookup"><span data-stu-id="5aa3f-106">PlaylistArray.item method</span></span>

<span data-ttu-id="5aa3f-107">El método **Item** recupera la lista de reproducción en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aa3f-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="5aa3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aa3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa3f-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5aa3f-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa3f-111">**Número** (**largo**) que contiene el índice de la lista de reproducción que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa3f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aa3f-112">Return value</span></span>

<span data-ttu-id="5aa3f-113">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="5aa3f-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa3f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa3f-114">Remarks</span></span>

<span data-ttu-id="5aa3f-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5aa3f-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5aa3f-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa3f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa3f-117">Requirements</span></span>



| <span data-ttu-id="5aa3f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa3f-118">Requirement</span></span> | <span data-ttu-id="5aa3f-119">Value</span><span class="sxs-lookup"><span data-stu-id="5aa3f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa3f-120">Versión</span><span class="sxs-lookup"><span data-stu-id="5aa3f-120">Version</span></span><br/> | <span data-ttu-id="5aa3f-121">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5aa3f-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aa3f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5aa3f-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa3f-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa3f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa3f-125">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="5aa3f-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="5aa3f-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5aa3f-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5aa3f-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5aa3f-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





