---
title: Propiedad visible (objeto Balloon)
description: Propiedad visible
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078673"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="e8b87-103">Propiedad visible (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="e8b87-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="e8b87-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8b87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e8b87-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="e8b87-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e8b87-106">Devuelve o establece el valor visible para el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="e8b87-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="e8b87-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="e8b87-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="e8b87-108">\*agente \***. Caracteres (**"\* CharacterID \*" \* *). Balloon. visible* \*  \[  =  *booleano*\]</span><span class="sxs-lookup"><span data-stu-id="e8b87-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="e8b87-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e8b87-109">Part</span></span>      | <span data-ttu-id="e8b87-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8b87-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b87-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e8b87-111">*boolean*</span></span> | <span data-ttu-id="e8b87-112">Una expresión booleana que especifica si el globo de palabras está visible.</span><span class="sxs-lookup"><span data-stu-id="e8b87-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="e8b87-113">**True** El globo está visible.</span><span class="sxs-lookup"><span data-stu-id="e8b87-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="e8b87-114">**False** El globo está oculto.</span><span class="sxs-lookup"><span data-stu-id="e8b87-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8b87-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8b87-115">Remarks</span></span>

<span data-ttu-id="e8b87-116">Si sigue una llamada de [**hablar**](speak-method.md) o de [**reflexión**](think-method.md) con una instrucción para intentar cambiar la propiedad del globo, es posible que no afecte al estado visible del globo porque la llamada de **Speak** o **pensar** se pone en cola, pero la llamada que establece el estado visible del globo no.</span><span class="sxs-lookup"><span data-stu-id="e8b87-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="e8b87-117">Por lo tanto, solo se establece este valor cuando no hay llamadas de **voz** o de **reflexión** en la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="e8b87-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="e8b87-118">Si intenta establecer esta propiedad mientras el carácter está hablando, moviendo o arrastrando, el valor de la propiedad no surtirá efecto hasta que se complete la operación anterior.</span><span class="sxs-lookup"><span data-stu-id="e8b87-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="e8b87-119">Llamar a los métodos [**Speak**](speak-method.md) y [**piénselo**](think-method.md) hace que el globo sea visible automáticamente, estableciendo la propiedad [**visible**](visible-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="e8b87-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="e8b87-120">Si la propiedad AutoHide de globos del carácter está habilitada, el globo se oculta automáticamente una vez que se habla del texto de salida.</span><span class="sxs-lookup"><span data-stu-id="e8b87-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="e8b87-121">Al hacer clic o arrastrar un carácter que no está hablando en ese momento, también se oculta automáticamente el globo incluso si su configuración de ocultación automática está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e8b87-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="e8b87-122">Puede cambiar la configuración de autoocultar del carácter mediante la propiedad de [**estilo**](style-property.md) del globo.</span><span class="sxs-lookup"><span data-stu-id="e8b87-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="e8b87-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8b87-123">See Also</span></span>

[<span data-ttu-id="e8b87-124">**Propiedad de estilo**</span><span class="sxs-lookup"><span data-stu-id="e8b87-124">**Style property**</span></span>](style-property.md)


 

 





