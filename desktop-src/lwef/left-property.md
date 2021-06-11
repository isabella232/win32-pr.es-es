---
title: Left (propiedad, objeto Characters)
description: Obtenga información sobre la propiedad de objeto Left Characters. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988941"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="910e3-104">Left (propiedad, objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="910e3-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="910e3-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="910e3-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="910e3-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="910e3-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="910e3-107">Devuelve o establece el borde izquierdo del marco del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="910e3-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="910e3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="910e3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="910e3-109">*agent\***. Caracteres ("**_CharacterID_*_"). Valor_ \*  \[  =  *izquierdo*\]</span><span class="sxs-lookup"><span data-stu-id="910e3-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="910e3-110">Parte</span><span class="sxs-lookup"><span data-stu-id="910e3-110">Part</span></span>    | <span data-ttu-id="910e3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="910e3-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="910e3-112">*value*</span><span class="sxs-lookup"><span data-stu-id="910e3-112">*value*</span></span> | <span data-ttu-id="910e3-113">Entero long que especifica el borde izquierdo del marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="910e3-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="910e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="910e3-114">Remarks</span></span>

<span data-ttu-id="910e3-115">La **propiedad Left** siempre se expresa en píxeles, en relación con el origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="910e3-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="910e3-116">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="910e3-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="910e3-117">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="910e3-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




