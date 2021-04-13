---
title: Propiedad visible (objeto Commands)
description: Propiedad visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421853"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="a9be9-103">Propiedad visible (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="a9be9-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="a9be9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9be9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a9be9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a9be9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a9be9-106">Devuelve o establece un valor que determina si el título de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="a9be9-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="a9be9-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a9be9-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="a9be9-108">\*agente \***. Caracteres (**"\* CharacterID \*" \* *). Commands. visible* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="a9be9-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="a9be9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a9be9-109">Part</span></span>      | <span data-ttu-id="a9be9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9be9-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9be9-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="a9be9-111">*boolean*</span></span> | <span data-ttu-id="a9be9-112">Expresión booleana que especifica si el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="a9be9-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="a9be9-113">**True** Aparece el título.</span><span class="sxs-lookup"><span data-stu-id="a9be9-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="a9be9-114">**False** El título no aparece.</span><span class="sxs-lookup"><span data-stu-id="a9be9-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9be9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9be9-115">Remarks</span></span>

<span data-ttu-id="a9be9-116">Para que el título aparezca en el menú emergente del carácter cuando la aplicación no es el cliente de entrada-activo, esta propiedad debe establecerse en **true** y en la propiedad [**Caption**](caption-property.md) establecida para la colección de comandos.</span><span class="sxs-lookup"><span data-stu-id="a9be9-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="a9be9-117">Además, esta propiedad debe establecerse en **true** para que los comandos de la colección aparezcan en el menú emergente cuando la aplicación sea de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="a9be9-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

