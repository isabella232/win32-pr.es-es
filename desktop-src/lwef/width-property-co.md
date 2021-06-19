---
title: Propiedad Width (objeto Characters)
description: Obtenga información sobre la propiedad Width del objeto Characters, que devuelve o establece el ancho del marco para el carácter especificado.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395131"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="dc483-103">Propiedad Width (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="dc483-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="dc483-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc483-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dc483-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc483-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dc483-106">Devuelve o establece el ancho del marco para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="dc483-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="dc483-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="dc483-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="dc483-108">*agent\***. Caracteres ("**_CharacterID_*_"). Valor de_ \*  \[ =  *ancho*\]</span><span class="sxs-lookup"><span data-stu-id="dc483-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="dc483-109">Parte</span><span class="sxs-lookup"><span data-stu-id="dc483-109">Part</span></span>    | <span data-ttu-id="dc483-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc483-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="dc483-111">*value*</span><span class="sxs-lookup"><span data-stu-id="dc483-111">*value*</span></span> | <span data-ttu-id="dc483-112">Entero Long que especifica el ancho del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="dc483-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc483-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc483-113">Remarks</span></span>

<span data-ttu-id="dc483-114">La [**propiedad Width**](width-property.md) siempre se expresa en píxeles.</span><span class="sxs-lookup"><span data-stu-id="dc483-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="dc483-115">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="dc483-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="dc483-116">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="dc483-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




