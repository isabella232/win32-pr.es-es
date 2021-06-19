---
title: Propiedad Visible (objeto Command)
description: Obtenga información sobre la propiedad Visible del objeto Command, que devuelve o establece si el comando está visible en el menú emergente del carácter.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396250"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="f1a18-103">Propiedad Visible (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="f1a18-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="f1a18-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1a18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f1a18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1a18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f1a18-106">Devuelve o establece si el [**comando**](/windows/desktop/lwef/the-command-object) está visible en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="f1a18-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f1a18-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="f1a18-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="f1a18-108">*agent\***. Characters(**"* CharacterID *"**). Commands(**"* name *"\*\*). Booleano* \*  \[  =  *visible*\]</span><span class="sxs-lookup"><span data-stu-id="f1a18-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="f1a18-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f1a18-109">Part</span></span>      | <span data-ttu-id="f1a18-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1a18-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a18-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f1a18-111">*boolean*</span></span> | <span data-ttu-id="f1a18-112">Expresión booleana que especifica si [**el**](/windows/desktop/lwef/the-command-object)título del comando aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="f1a18-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="f1a18-113">**True** (valor predeterminado) Aparece el título.</span><span class="sxs-lookup"><span data-stu-id="f1a18-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="f1a18-114">**False** El título no aparece.</span><span class="sxs-lookup"><span data-stu-id="f1a18-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1a18-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1a18-115">Remarks</span></span>

<span data-ttu-id="f1a18-116">Establezca esta propiedad en **False** cuando quiera incluir la entrada de voz para sus propias interfaces sin que aparezcan en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="f1a18-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="f1a18-117">Si establece [](/windows/desktop/lwef/the-command-object) la propiedad [**Caption**](caption-property.md) de un objeto Command en la cadena vacía (""), el texto del título no aparecerá en el menú emergente (por ejemplo, como una línea en blanco), independientemente de su configuración de propiedad [**Visible.**](visible-property.md)</span><span class="sxs-lookup"><span data-stu-id="f1a18-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="f1a18-118">El [**valor de**](visible-property.md) la propiedad Visible de la colección [**Commands**](/windows/desktop/lwef/the-command-object) primaria de un objeto [**Command**](/windows/desktop/lwef/the-commands-collection-object) no afecta al valor de propiedad **Visible** del **comando**.</span><span class="sxs-lookup"><span data-stu-id="f1a18-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

