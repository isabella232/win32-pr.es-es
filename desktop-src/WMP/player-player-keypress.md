---
title: Evento Player. KeyPress
description: El evento KeyPress tiene lugar cuando se presiona y se suelta una tecla. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Media Player de eventos KeyPress de Windows
- Evento KeyPress Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708653"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="73a6d-107">Evento Player. KeyPress</span><span class="sxs-lookup"><span data-stu-id="73a6d-107">Player.KeyPress event</span></span>

<span data-ttu-id="73a6d-108">El evento **KeyPress** tiene lugar cuando se presiona y se suelta una tecla.</span><span class="sxs-lookup"><span data-stu-id="73a6d-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a6d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73a6d-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="73a6d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73a6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a6d-111">*nKeyAscii*</span><span class="sxs-lookup"><span data-stu-id="73a6d-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="73a6d-112">**Número** (**int**) que especifica el código ANSI numérico estándar para el carácter.</span><span class="sxs-lookup"><span data-stu-id="73a6d-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a6d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73a6d-113">Return value</span></span>

<span data-ttu-id="73a6d-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="73a6d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a6d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73a6d-115">Remarks</span></span>

<span data-ttu-id="73a6d-116">Este evento se produce cuando el resultado de la pulsación de tecla es cualquier carácter imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de unos pocos caracteres especiales, y la tecla entrar o retroceso.</span><span class="sxs-lookup"><span data-stu-id="73a6d-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="73a6d-117">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="73a6d-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="73a6d-118">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73a6d-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="73a6d-119">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="73a6d-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="73a6d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73a6d-120">Requirements</span></span>



| <span data-ttu-id="73a6d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a6d-121">Requirement</span></span> | <span data-ttu-id="73a6d-122">Value</span><span class="sxs-lookup"><span data-stu-id="73a6d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73a6d-123">Versión</span><span class="sxs-lookup"><span data-stu-id="73a6d-123">Version</span></span><br/> | <span data-ttu-id="73a6d-124">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="73a6d-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="73a6d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73a6d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="73a6d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a6d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a6d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="73a6d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a6d-128">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="73a6d-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





