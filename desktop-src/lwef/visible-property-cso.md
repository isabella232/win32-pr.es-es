---
title: Propiedad Visible (objeto Commands)
description: Obtenga información sobre la propiedad Visible del objeto Commands, que determina si el título de la colección Commands aparece en el menú emergente del carácter.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396260"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="6e03e-103">Propiedad Visible (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="6e03e-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="6e03e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6e03e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6e03e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e03e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6e03e-106">Devuelve o establece un valor que determina si el título de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="6e03e-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="6e03e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6e03e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="6e03e-108">*agent\***. Characters(**"* CharacterID *"\*\*). Commands.Visible* \*  \[  =  *boolean*\]</span><span class="sxs-lookup"><span data-stu-id="6e03e-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="6e03e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6e03e-109">Part</span></span>      | <span data-ttu-id="6e03e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e03e-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e03e-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="6e03e-111">*boolean*</span></span> | <span data-ttu-id="6e03e-112">Expresión booleana que especifica si el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="6e03e-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="6e03e-113">**True** Aparece el título.</span><span class="sxs-lookup"><span data-stu-id="6e03e-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="6e03e-114">**False** El título no aparece.</span><span class="sxs-lookup"><span data-stu-id="6e03e-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e03e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e03e-115">Remarks</span></span>

<span data-ttu-id="6e03e-116">Para que el título aparezca en el menú emergente del carácter cuando la aplicación no sea el cliente activo de entrada, esta propiedad debe establecerse en **True** y la propiedad [**Caption**](caption-property.md) para la colección Commands.</span><span class="sxs-lookup"><span data-stu-id="6e03e-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="6e03e-117">Además, esta propiedad debe establecerse en **True** para que los comandos de la colección aparezcan en el menú emergente cuando la aplicación esté activa en la entrada.</span><span class="sxs-lookup"><span data-stu-id="6e03e-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

