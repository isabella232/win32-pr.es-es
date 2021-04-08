---
title: Propiedad width (objeto Characters)
description: Width (propiedad)
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078722"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="0225a-103">Propiedad width (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="0225a-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="0225a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0225a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0225a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="0225a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0225a-106">Devuelve o establece el ancho del marco para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="0225a-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="0225a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="0225a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="0225a-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \*  \[ =  *Valor* de ancho\]</span><span class="sxs-lookup"><span data-stu-id="0225a-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="0225a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0225a-109">Part</span></span>    | <span data-ttu-id="0225a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0225a-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="0225a-111">*value*</span><span class="sxs-lookup"><span data-stu-id="0225a-111">*value*</span></span> | <span data-ttu-id="0225a-112">Entero largo que especifica el ancho del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="0225a-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0225a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0225a-113">Remarks</span></span>

<span data-ttu-id="0225a-114">La propiedad [**ancho**](width-property.md) siempre se expresa en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0225a-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="0225a-115">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="0225a-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="0225a-116">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0225a-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




