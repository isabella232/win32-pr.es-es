---
title: Evento Player. CdromMediaChange
description: El evento CdromMediaChange se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Media Player CdromMediaChange de eventos de Windows
- Evento CdromMediaChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708763"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="1392e-107">Evento Player. CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="1392e-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="1392e-108">El evento **CdromMediaChange** se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="1392e-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1392e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1392e-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="1392e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1392e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1392e-111">*CdromNum*</span><span class="sxs-lookup"><span data-stu-id="1392e-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="1392e-112">**Número** (**largo**) que especifica el índice de la unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="1392e-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1392e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1392e-113">Return value</span></span>

<span data-ttu-id="1392e-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1392e-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1392e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1392e-115">Remarks</span></span>

<span data-ttu-id="1392e-116">El índice de la unidad de CD corresponde al índice de un objeto **CDROM** en **CdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="1392e-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="1392e-117">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="1392e-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1392e-118">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1392e-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1392e-119">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="1392e-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1392e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1392e-120">Requirements</span></span>



| <span data-ttu-id="1392e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1392e-121">Requirement</span></span> | <span data-ttu-id="1392e-122">Value</span><span class="sxs-lookup"><span data-stu-id="1392e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1392e-123">Versión</span><span class="sxs-lookup"><span data-stu-id="1392e-123">Version</span></span><br/> | <span data-ttu-id="1392e-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1392e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1392e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1392e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1392e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1392e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1392e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1392e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1392e-128">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="1392e-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="1392e-129">**Objeto CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="1392e-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="1392e-130">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="1392e-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





