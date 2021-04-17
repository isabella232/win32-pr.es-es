---
title: Propiedad visible (objeto Characters)
description: Propiedad visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695812"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="1be88-103">Propiedad visible (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="1be88-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="1be88-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1be88-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1be88-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="1be88-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1be88-106">Devuelve un valor booleano que indica si el carácter está visible.</span><span class="sxs-lookup"><span data-stu-id="1be88-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="1be88-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="1be88-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="1be88-108">\*agente \***. Caracteres (**"\* CharacterID *" \* *). Visible**</span><span class="sxs-lookup"><span data-stu-id="1be88-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="1be88-109">Value</span><span class="sxs-lookup"><span data-stu-id="1be88-109">Value</span></span> | <span data-ttu-id="1be88-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1be88-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="1be88-111">True</span><span class="sxs-lookup"><span data-stu-id="1be88-111">True</span></span>  | <span data-ttu-id="1be88-112">Se muestra el carácter.</span><span class="sxs-lookup"><span data-stu-id="1be88-112">The character is displayed.</span></span>            |
| <span data-ttu-id="1be88-113">False</span><span class="sxs-lookup"><span data-stu-id="1be88-113">False</span></span> | <span data-ttu-id="1be88-114">El carácter está oculto (no es visible).</span><span class="sxs-lookup"><span data-stu-id="1be88-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1be88-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1be88-115">Remarks</span></span>

<span data-ttu-id="1be88-116">Esta propiedad indica si se muestra el fotograma del carácter.</span><span class="sxs-lookup"><span data-stu-id="1be88-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="1be88-117">No significa necesariamente que haya una imagen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1be88-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="1be88-118">Por ejemplo, esta propiedad devuelve **true** incluso cuando el carácter se coloca fuera del área de visualización visible o cuando el marco de carácter actual no contiene ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="1be88-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="1be88-119">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="1be88-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="1be88-120">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1be88-120">This property is read-only.</span></span> <span data-ttu-id="1be88-121">Para hacer que un carácter esté visible u oculto, use los métodos [**Mostrar**](show-method.md) u [**ocultar**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="1be88-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




