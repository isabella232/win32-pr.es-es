---
title: Evento Player. MediaError
description: El evento MediaError se produce cuando el objeto multimedia tiene una condición de error.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player MediaError de eventos de Windows
- Evento MediaError de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709007"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="cd206-106">Evento Player. MediaError</span><span class="sxs-lookup"><span data-stu-id="cd206-106">Player.MediaError event</span></span>

<span data-ttu-id="cd206-107">El evento **MediaError** se produce cuando el objeto **multimedia** tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="cd206-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd206-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd206-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="cd206-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd206-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd206-110">*pMediaObject*</span><span class="sxs-lookup"><span data-stu-id="cd206-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="cd206-111">Objeto **multimedia** que tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="cd206-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd206-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd206-112">Return value</span></span>

<span data-ttu-id="cd206-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="cd206-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd206-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd206-114">Remarks</span></span>

<span data-ttu-id="cd206-115">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="cd206-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="cd206-116">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cd206-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd206-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd206-117">Requirements</span></span>



| <span data-ttu-id="cd206-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd206-118">Requirement</span></span> | <span data-ttu-id="cd206-119">Value</span><span class="sxs-lookup"><span data-stu-id="cd206-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd206-120">Versión</span><span class="sxs-lookup"><span data-stu-id="cd206-120">Version</span></span><br/> | <span data-ttu-id="cd206-121">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="cd206-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="cd206-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd206-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd206-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd206-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd206-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd206-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd206-125">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="cd206-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





