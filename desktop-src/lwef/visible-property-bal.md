---
title: Propiedad Visible (objeto De globo)
description: Obtenga información sobre la propiedad Visible del objeto Globo, que devuelve o establece la configuración visible para el globo de palabras para el carácter especificado.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396330"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="a336b-103">Propiedad Visible (objeto De globo)</span><span class="sxs-lookup"><span data-stu-id="a336b-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="a336b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a336b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a336b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a336b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a336b-106">Devuelve o establece la configuración visible para el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="a336b-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a336b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="a336b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="a336b-108">*agent\***. Characters(**"* CharacterID *"\*\*). Booleano Balloon.Visible* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="a336b-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="a336b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a336b-109">Part</span></span>      | <span data-ttu-id="a336b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a336b-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a336b-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="a336b-111">*boolean*</span></span> | <span data-ttu-id="a336b-112">Expresión booleana que especifica si el globo de palabras está visible.</span><span class="sxs-lookup"><span data-stu-id="a336b-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="a336b-113">**True** El globo está visible.</span><span class="sxs-lookup"><span data-stu-id="a336b-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="a336b-114">**False** El globo está oculto.</span><span class="sxs-lookup"><span data-stu-id="a336b-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a336b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a336b-115">Remarks</span></span>

<span data-ttu-id="a336b-116">Si sigue [](speak-method.md) una llamada a Speak o [**Think**](think-method.md) con una instrucción para intentar cambiar la propiedad del  globo, es posible que no afecte al estado Visible del globo porque la llamada Speak o **Think** se pone en cola, pero la llamada que establece el estado visible del globo no.</span><span class="sxs-lookup"><span data-stu-id="a336b-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="a336b-117">Por lo tanto, establezca este valor solo cuando no haya llamadas **speak** o **think** en la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="a336b-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="a336b-118">Si intenta establecer esta propiedad mientras el carácter habla, se mueve o se arrastra, la configuración de la propiedad no tiene efecto hasta que se completa la operación anterior.</span><span class="sxs-lookup"><span data-stu-id="a336b-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="a336b-119">Llamar a [**los métodos Speak**](speak-method.md) y [**Think**](think-method.md) automáticamente hace que el globo sea visible, estableciendo la [**propiedad Visible**](visible-property.md) en **True.**</span><span class="sxs-lookup"><span data-stu-id="a336b-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="a336b-120">Si la propiedad AutoHide del globo del carácter está habilitada, el globo se oculta automáticamente después de que se hable el texto de salida.</span><span class="sxs-lookup"><span data-stu-id="a336b-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="a336b-121">Al hacer clic o arrastrar un carácter que no está hablando actualmente, también se oculta automáticamente el globo aunque su configuración Detección automática esté deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="a336b-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="a336b-122">Puede cambiar la configuración de AutoHide del carácter mediante la propiedad [**Style del**](style-property.md) globo.</span><span class="sxs-lookup"><span data-stu-id="a336b-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="a336b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a336b-123">See Also</span></span>

[<span data-ttu-id="a336b-124">**Propiedad Style**</span><span class="sxs-lookup"><span data-stu-id="a336b-124">**Style property**</span></span>](style-property.md)


 

 





