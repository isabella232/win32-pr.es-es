---
title: Propiedad Top (objeto Characters)
description: Obtenga información sobre la propiedad Top (objeto Characters). Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396350"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="12a80-104">Propiedad Top (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="12a80-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="12a80-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12a80-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="12a80-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12a80-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="12a80-107">Devuelve o establece el borde superior del marco del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="12a80-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="12a80-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="12a80-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="12a80-109">*agent\***. Caracteres ("**_CharacterID_*_"). Valor_ \*  \[  =  *superior*\]</span><span class="sxs-lookup"><span data-stu-id="12a80-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="12a80-110">Parte</span><span class="sxs-lookup"><span data-stu-id="12a80-110">Part</span></span>    | <span data-ttu-id="12a80-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="12a80-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="12a80-112">*value*</span><span class="sxs-lookup"><span data-stu-id="12a80-112">*value*</span></span> | <span data-ttu-id="12a80-113">Entero Long que especifica el borde superior del carácter.</span><span class="sxs-lookup"><span data-stu-id="12a80-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12a80-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12a80-114">Remarks</span></span>

<span data-ttu-id="12a80-115">La **propiedad Top** siempre se expresa en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="12a80-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="12a80-116">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="12a80-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="12a80-117">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="12a80-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="12a80-118">Use el [**método MoveTo**](moveto-method.md) para cambiar la ubicación del carácter.</span><span class="sxs-lookup"><span data-stu-id="12a80-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="12a80-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12a80-119">See Also</span></span>

<span data-ttu-id="12a80-120">[**Left, propiedad**](left-property.md), [ **método MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="12a80-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




