---
title: Propiedad top (objeto Characters)
description: Propiedad Top
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714515"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="1ef5c-103">Propiedad top (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="1ef5c-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="1ef5c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ef5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1ef5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="1ef5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1ef5c-106">Devuelve o establece el borde superior del marco del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="1ef5c-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="1ef5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="1ef5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1ef5c-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \*  \[  =  *Valor* superior\]</span><span class="sxs-lookup"><span data-stu-id="1ef5c-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="1ef5c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1ef5c-109">Part</span></span>    | <span data-ttu-id="1ef5c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef5c-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="1ef5c-111">*value*</span><span class="sxs-lookup"><span data-stu-id="1ef5c-111">*value*</span></span> | <span data-ttu-id="1ef5c-112">Entero largo que especifica el borde superior del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ef5c-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ef5c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ef5c-113">Remarks</span></span>

<span data-ttu-id="1ef5c-114">La propiedad **Top** siempre se expresa en píxeles, en relación con el origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="1ef5c-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="1ef5c-115">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ef5c-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="1ef5c-116">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ef5c-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="1ef5c-117">Utilice el método [**moveTo**](moveto-method.md) para cambiar la ubicación del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ef5c-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ef5c-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ef5c-118">See Also</span></span>

<span data-ttu-id="1ef5c-119">[**Propiedad Left**](left-property.md), [ **método moveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="1ef5c-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




