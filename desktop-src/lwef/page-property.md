---
title: Propiedad de página
description: Propiedad de página
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418684"
---
# <a name="page-property"></a><span data-ttu-id="4b704-103">Propiedad de página</span><span class="sxs-lookup"><span data-stu-id="4b704-103">Page Property</span></span>

<span data-ttu-id="4b704-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b704-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4b704-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="4b704-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4b704-106">Devuelve o establece la página mostrada en la ventana de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4b704-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="4b704-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="4b704-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="4b704-108">\*agente \* \* *.* \*  \[  =  *Cadena* PropertySheet.Page\]</span><span class="sxs-lookup"><span data-stu-id="4b704-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="4b704-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4b704-109">Part</span></span>     | <span data-ttu-id="4b704-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b704-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b704-111">*string*</span><span class="sxs-lookup"><span data-stu-id="4b704-111">*string*</span></span> | <span data-ttu-id="4b704-112">Expresión de cadena con uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b704-112">A string expression with one of the following values.</span></span> <span data-ttu-id="4b704-113">**"Voz"** Muestra la página de entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="4b704-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="4b704-114">**"Output"** Muestra la página de salida.</span><span class="sxs-lookup"><span data-stu-id="4b704-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="4b704-115">**"Copyright"** Muestra la página de copyright.</span><span class="sxs-lookup"><span data-stu-id="4b704-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b704-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b704-116">Remarks</span></span>

<span data-ttu-id="4b704-117">Si no hay instalado ningún motor de voz, el establecimiento de la **Página** en **"voz"** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="4b704-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="4b704-118">Además, la propiedad **visible** de la ventana debe establecerse en **true** para que el usuario vea la página.</span><span class="sxs-lookup"><span data-stu-id="4b704-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="4b704-119">El usuario puede invalidar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4b704-119">The user can override this property.</span></span>

 

 

 





