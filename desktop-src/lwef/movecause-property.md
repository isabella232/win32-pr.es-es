---
title: Propiedad MoveCause
description: Propiedad MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903507"
---
# <a name="movecause-property"></a><span data-ttu-id="32e95-103">Propiedad MoveCause</span><span class="sxs-lookup"><span data-stu-id="32e95-103">MoveCause Property</span></span>

<span data-ttu-id="32e95-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32e95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="32e95-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="32e95-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="32e95-106">Devuelve un valor entero que especifica la causa del último movimiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="32e95-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="32e95-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="32e95-108">*agente*. **Caracteres ("***CharacterID***"). MoveCause**</span><span class="sxs-lookup"><span data-stu-id="32e95-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="32e95-109">Value</span><span class="sxs-lookup"><span data-stu-id="32e95-109">Value</span></span> | <span data-ttu-id="32e95-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="32e95-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e95-111">0</span><span class="sxs-lookup"><span data-stu-id="32e95-111">0</span></span>     | <span data-ttu-id="32e95-112">No se ha despasado el carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="32e95-113">1</span><span class="sxs-lookup"><span data-stu-id="32e95-113">1</span></span>     | <span data-ttu-id="32e95-114">El usuario ha despasado el carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="32e95-115">2</span><span class="sxs-lookup"><span data-stu-id="32e95-115">2</span></span>     | <span data-ttu-id="32e95-116">La aplicación ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="32e95-117">3</span><span class="sxs-lookup"><span data-stu-id="32e95-117">3</span></span>     | <span data-ttu-id="32e95-118">Otra aplicación cliente ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="32e95-119">4</span><span class="sxs-lookup"><span data-stu-id="32e95-119">4</span></span>     | <span data-ttu-id="32e95-120">El servidor del agente ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="32e95-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32e95-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32e95-121">Remarks</span></span>

<span data-ttu-id="32e95-122">Puede usar esta propiedad para determinar qué causó el movimiento del carácter, cuando más de una aplicación comparte (ha cargado) el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="32e95-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="32e95-123">Estos valores son los mismos que los devueltos por el evento de [**movimiento**](move-event.md) .</span><span class="sxs-lookup"><span data-stu-id="32e95-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="32e95-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32e95-124">See Also</span></span>

<span data-ttu-id="32e95-125">[**Evento Move**](move-event.md), [ **método moveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="32e95-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




