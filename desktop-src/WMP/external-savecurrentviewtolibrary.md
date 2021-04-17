---
title: External. saveCurrentViewToLibrary (método)
description: El método saveCurrentViewToLibrary crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- método saveCurrentViewToLibrary de Windows Media Player
- método saveCurrentViewToLibrary de Windows Media Player, clase externa
- Clase externa Windows Media Player, método saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698579"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="5ca12-106">External. saveCurrentViewToLibrary (método)</span><span class="sxs-lookup"><span data-stu-id="5ca12-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="5ca12-107">El método **saveCurrentViewToLibrary** crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="5ca12-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca12-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ca12-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="5ca12-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ca12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca12-110">*FriendlyListName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ca12-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca12-111">**Cadena** que especifica un nombre descriptivo para la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5ca12-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="5ca12-112">Windows Media Player muestra este nombre en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ca12-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="5ca12-113">*Local* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ca12-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca12-114">**Valor booleano** que especifica si la lista de reproducción es dinámica o estática.</span><span class="sxs-lookup"><span data-stu-id="5ca12-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="5ca12-115">**True** especifica Dynamic y **false** especifica static.</span><span class="sxs-lookup"><span data-stu-id="5ca12-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca12-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ca12-116">Return value</span></span>

<span data-ttu-id="5ca12-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5ca12-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca12-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ca12-118">Requirements</span></span>



| <span data-ttu-id="5ca12-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ca12-119">Requirement</span></span> | <span data-ttu-id="5ca12-120">Value</span><span class="sxs-lookup"><span data-stu-id="5ca12-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca12-121">Versión</span><span class="sxs-lookup"><span data-stu-id="5ca12-121">Version</span></span><br/> | <span data-ttu-id="5ca12-122">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="5ca12-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="5ca12-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ca12-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ca12-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca12-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca12-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ca12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca12-126">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5ca12-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





