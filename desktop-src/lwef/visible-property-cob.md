---
title: Propiedad Visible (objeto Characters)
description: Obtenga información sobre la propiedad Visible del objeto Characters, que devuelve un valor booleano que indica si el carácter está visible.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396310"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="7c09e-103">Propiedad Visible (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="7c09e-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="7c09e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c09e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7c09e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c09e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7c09e-106">Devuelve un valor booleano que indica si el carácter está visible.</span><span class="sxs-lookup"><span data-stu-id="7c09e-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="7c09e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="7c09e-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="7c09e-108">*agent\***. Characters(**"* CharacterID *"\*\*). Visible*\*</span><span class="sxs-lookup"><span data-stu-id="7c09e-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="7c09e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7c09e-109">Value</span></span> | <span data-ttu-id="7c09e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c09e-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="7c09e-111">True</span><span class="sxs-lookup"><span data-stu-id="7c09e-111">True</span></span>  | <span data-ttu-id="7c09e-112">Se muestra el carácter .</span><span class="sxs-lookup"><span data-stu-id="7c09e-112">The character is displayed.</span></span>            |
| <span data-ttu-id="7c09e-113">False</span><span class="sxs-lookup"><span data-stu-id="7c09e-113">False</span></span> | <span data-ttu-id="7c09e-114">El carácter está oculto (no visible).</span><span class="sxs-lookup"><span data-stu-id="7c09e-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c09e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c09e-115">Remarks</span></span>

<span data-ttu-id="7c09e-116">Esta propiedad indica si se muestra el marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="7c09e-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="7c09e-117">No significa necesariamente que haya una imagen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7c09e-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="7c09e-118">Por ejemplo, esta propiedad devuelve **True** incluso cuando el carácter se coloca fuera del área de visualización visible o cuando el marco de caracteres actual no contiene imágenes.</span><span class="sxs-lookup"><span data-stu-id="7c09e-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="7c09e-119">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="7c09e-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="7c09e-120">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7c09e-120">This property is read-only.</span></span> <span data-ttu-id="7c09e-121">Para que un carácter sea visible u oculto, use los [**métodos Show**](show-method.md) [**u Hide.**](https://www.bing.com/search?q=**Hide**)</span><span class="sxs-lookup"><span data-stu-id="7c09e-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




