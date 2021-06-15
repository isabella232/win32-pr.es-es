---
title: Propiedad Height (objeto Characters)
description: Obtenga información sobre la propiedad Height del objeto Characters. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068520"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="15ad1-104">Propiedad Height (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="15ad1-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="15ad1-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15ad1-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="15ad1-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15ad1-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="15ad1-107">Devuelve o establece el alto del marco del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="15ad1-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="15ad1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="15ad1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="15ad1-109">*agent\***. Caracteres ("**_CharacterID_*_"). Valor de_ \*  \[ =  *alto*\]</span><span class="sxs-lookup"><span data-stu-id="15ad1-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="15ad1-110">Parte</span><span class="sxs-lookup"><span data-stu-id="15ad1-110">Part</span></span>    | <span data-ttu-id="15ad1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="15ad1-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="15ad1-112">*value*</span><span class="sxs-lookup"><span data-stu-id="15ad1-112">*value*</span></span> | <span data-ttu-id="15ad1-113">Entero Long que especifica el alto del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="15ad1-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15ad1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15ad1-114">Remarks</span></span>

<span data-ttu-id="15ad1-115">La **propiedad Height** siempre se expresa en píxeles, en relación con las coordenadas de pantalla (esquina superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="15ad1-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="15ad1-116">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="15ad1-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="15ad1-117">Aunque el carácter aparece en una ventana de región con forma irregular, el alto del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15ad1-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




