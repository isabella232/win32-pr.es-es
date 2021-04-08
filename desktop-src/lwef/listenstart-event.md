---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903796"
---
# <a name="listenstart-event"></a><span data-ttu-id="abc4e-103">Evento ListenStart</span><span class="sxs-lookup"><span data-stu-id="abc4e-103">ListenStart Event</span></span>

<span data-ttu-id="abc4e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="abc4e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="abc4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="abc4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="abc4e-106">Se produce cuando comienza el modo de escucha (reconocimiento de voz).</span><span class="sxs-lookup"><span data-stu-id="abc4e-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="abc4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="abc4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="abc4e-108">**Sub** *Agent. \* \* \* ListenStart (ByVal* \*  \*CharacterID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="abc4e-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="abc4e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="abc4e-109">Part</span></span>          | <span data-ttu-id="abc4e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="abc4e-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="abc4e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="abc4e-111">*CharacterID*</span></span> | <span data-ttu-id="abc4e-112">Devuelve el identificador del carácter de escucha como una cadena.</span><span class="sxs-lookup"><span data-stu-id="abc4e-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="abc4e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abc4e-113">Remarks</span></span>

<span data-ttu-id="abc4e-114">Este evento se envía a todos los clientes cuando comienza el modo de escucha porque el usuario presionó la clave de escucha o el cliente de entrada-activo llamó al método [**Listen**](listen-method.md) con **true**.</span><span class="sxs-lookup"><span data-stu-id="abc4e-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="abc4e-115">Puede usar este evento para evitar que el personaje hable mientras el modo de escucha está activado.</span><span class="sxs-lookup"><span data-stu-id="abc4e-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="abc4e-116">Si activa el modo de escucha con el método [**Listen**](listen-method.md) y el usuario presiona la tecla de escucha, el modo de escucha se restablece y continúa hasta que se completa el tiempo de espera de la clave de escucha, se libera la clave de escucha o el usuario termina de hablar, lo que sea posterior.</span><span class="sxs-lookup"><span data-stu-id="abc4e-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="abc4e-117">En esta situación, cuando el modo de escucha ya está activado, no recibirá un evento **ListenStart** adicional cuando el usuario presione la tecla de escucha.</span><span class="sxs-lookup"><span data-stu-id="abc4e-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="abc4e-118">El evento devuelve el carácter a los clientes que actualmente tienen este carácter cargado.</span><span class="sxs-lookup"><span data-stu-id="abc4e-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="abc4e-119">El resto de clientes reciben un carácter nulo (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="abc4e-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="abc4e-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="abc4e-120">See Also</span></span>

<span data-ttu-id="abc4e-121">[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="abc4e-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




