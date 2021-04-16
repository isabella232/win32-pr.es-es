---
title: Propiedad visible (objeto Command)
description: Propiedad visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714505"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="0db67-103">Propiedad visible (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="0db67-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="0db67-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0db67-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0db67-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="0db67-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0db67-106">Devuelve o establece si el [**comando**](/windows/desktop/lwef/the-command-object) está visible en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="0db67-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="0db67-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="0db67-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="0db67-108">\*agente \***. Caracteres (**"\* CharacterID *"**). Comandos (**"* name \*" \* *).* \*  \[  =  *Booleano* visible\]</span><span class="sxs-lookup"><span data-stu-id="0db67-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="0db67-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0db67-109">Part</span></span>      | <span data-ttu-id="0db67-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0db67-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db67-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="0db67-111">*boolean*</span></span> | <span data-ttu-id="0db67-112">Una expresión booleana que especifica si el título del [**comando**](/windows/desktop/lwef/the-command-object)aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="0db67-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="0db67-113">**True** (valor predeterminado) aparece el título.</span><span class="sxs-lookup"><span data-stu-id="0db67-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="0db67-114">**False** El título no aparece.</span><span class="sxs-lookup"><span data-stu-id="0db67-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0db67-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0db67-115">Remarks</span></span>

<span data-ttu-id="0db67-116">Establezca esta propiedad en **false** si desea incluir la entrada de voz para sus propias interfaces sin que aparezcan en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="0db67-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="0db67-117">Si establece la propiedad [**título**](caption-property.md) de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la cadena vacía (""), el texto del título no aparecerá en el menú emergente (por ejemplo, como una línea en blanco), independientemente de su configuración de propiedad [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0db67-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="0db67-118">El valor de la propiedad [**visible**](visible-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) primarios de un objeto [**Command**](/windows/desktop/lwef/the-command-object) no afecta al valor de la propiedad **visible** del **comando**.</span><span class="sxs-lookup"><span data-stu-id="0db67-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

