---
title: Propiedad height (objeto Characters)
description: Height (propiedad)
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800643"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="c5e2d-103">Propiedad height (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="c5e2d-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="c5e2d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5e2d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c5e2d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="c5e2d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c5e2d-106">Devuelve o establece el alto del fotograma del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="c5e2d-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="c5e2d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="c5e2d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c5e2d-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \*  \[ =  *Valor* de alto\]</span><span class="sxs-lookup"><span data-stu-id="c5e2d-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="c5e2d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c5e2d-109">Part</span></span>    | <span data-ttu-id="c5e2d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5e2d-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="c5e2d-111">*value*</span><span class="sxs-lookup"><span data-stu-id="c5e2d-111">*value*</span></span> | <span data-ttu-id="c5e2d-112">Entero largo que especifica el alto del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="c5e2d-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5e2d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5e2d-113">Remarks</span></span>

<span data-ttu-id="c5e2d-114">La propiedad **height** siempre se expresa en píxeles, con respecto a las coordenadas de pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="c5e2d-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="c5e2d-115">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="c5e2d-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="c5e2d-116">Aunque el carácter aparece en una ventana de región con forma irregular, el alto del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5e2d-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




