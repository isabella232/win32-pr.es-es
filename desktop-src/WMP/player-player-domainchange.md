---
title: Evento Player. DomainChange
description: El evento DomainChange se produce cuando cambia el dominio del DVD. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Media Player DomainChange de eventos de Windows
- Evento DomainChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708966"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="5de7d-107">Evento Player. DomainChange</span><span class="sxs-lookup"><span data-stu-id="5de7d-107">Player.DomainChange event</span></span>

<span data-ttu-id="5de7d-108">El evento **DomainChange** se produce cuando cambia el dominio del DVD.</span><span class="sxs-lookup"><span data-stu-id="5de7d-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de7d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5de7d-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="5de7d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5de7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de7d-111">*strDomain*</span><span class="sxs-lookup"><span data-stu-id="5de7d-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="5de7d-112">**Cadena** que indica el nuevo dominio.</span><span class="sxs-lookup"><span data-stu-id="5de7d-112">**String** indicating the new domain.</span></span> <span data-ttu-id="5de7d-113">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5de7d-113">Contains one of the following values.</span></span>



| <span data-ttu-id="5de7d-114">String</span><span class="sxs-lookup"><span data-stu-id="5de7d-114">String</span></span>            | <span data-ttu-id="5de7d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5de7d-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="5de7d-116">firstplay</span><span class="sxs-lookup"><span data-stu-id="5de7d-116">firstplay</span></span>         | <span data-ttu-id="5de7d-117">Realizar la inicialización predeterminada de un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="5de7d-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="5de7d-118">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="5de7d-118">videoManagerMenu</span></span>  | <span data-ttu-id="5de7d-119">Mostrando menús para todo el disco. También se conoce como menú o menú raíz.</span><span class="sxs-lookup"><span data-stu-id="5de7d-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="5de7d-120">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="5de7d-120">videoTitleSetMenu</span></span> | <span data-ttu-id="5de7d-121">Mostrar menús para el conjunto de títulos actual.</span><span class="sxs-lookup"><span data-stu-id="5de7d-121">Displaying menus for current title set.</span></span> <span data-ttu-id="5de7d-122">También se conoce como titleMenu.</span><span class="sxs-lookup"><span data-stu-id="5de7d-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="5de7d-123">title</span><span class="sxs-lookup"><span data-stu-id="5de7d-123">title</span></span>             | <span data-ttu-id="5de7d-124">Mostrar el título actual.</span><span class="sxs-lookup"><span data-stu-id="5de7d-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="5de7d-125">stop</span><span class="sxs-lookup"><span data-stu-id="5de7d-125">stop</span></span>              | <span data-ttu-id="5de7d-126">El navegador de DVD está en el dominio de detención de DVD.</span><span class="sxs-lookup"><span data-stu-id="5de7d-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de7d-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5de7d-127">Return value</span></span>

<span data-ttu-id="5de7d-128">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5de7d-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de7d-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5de7d-129">Remarks</span></span>

<span data-ttu-id="5de7d-130">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="5de7d-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5de7d-131">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5de7d-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5de7d-132">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="5de7d-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5de7d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5de7d-133">Requirements</span></span>



| <span data-ttu-id="5de7d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de7d-134">Requirement</span></span> | <span data-ttu-id="5de7d-135">Value</span><span class="sxs-lookup"><span data-stu-id="5de7d-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5de7d-136">Versión</span><span class="sxs-lookup"><span data-stu-id="5de7d-136">Version</span></span><br/> | <span data-ttu-id="5de7d-137">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="5de7d-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="5de7d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5de7d-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="5de7d-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5de7d-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de7d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5de7d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de7d-141">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="5de7d-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="5de7d-142">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="5de7d-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





