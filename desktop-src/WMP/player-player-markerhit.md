---
title: Evento Player. MarkerHit
description: El evento MarkerHit se produce cuando se alcanza un marcador. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player MarkerHit de eventos de Windows
- Evento MarkerHit de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690184"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="bd875-107">Evento Player. MarkerHit</span><span class="sxs-lookup"><span data-stu-id="bd875-107">Player.MarkerHit event</span></span>

<span data-ttu-id="bd875-108">El evento **MarkerHit** se produce cuando se alcanza un marcador.</span><span class="sxs-lookup"><span data-stu-id="bd875-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd875-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd875-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="bd875-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd875-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd875-111">*MarkerNum*</span><span class="sxs-lookup"><span data-stu-id="bd875-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="bd875-112">**Número** (**largo**) que indica el número del marcador que se alcanzó.</span><span class="sxs-lookup"><span data-stu-id="bd875-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd875-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd875-113">Return value</span></span>

<span data-ttu-id="bd875-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="bd875-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd875-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd875-115">Remarks</span></span>

<span data-ttu-id="bd875-116">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="bd875-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="bd875-117">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bd875-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd875-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd875-118">Requirements</span></span>



| <span data-ttu-id="bd875-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd875-119">Requirement</span></span> | <span data-ttu-id="bd875-120">Value</span><span class="sxs-lookup"><span data-stu-id="bd875-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd875-121">Versión</span><span class="sxs-lookup"><span data-stu-id="bd875-121">Version</span></span><br/> | <span data-ttu-id="bd875-122">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bd875-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bd875-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd875-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bd875-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd875-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd875-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd875-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd875-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="bd875-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





