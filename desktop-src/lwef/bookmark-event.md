---
title: Bookmark (evento)
description: Bookmark (evento)
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268613"
---
# <a name="bookmark-event"></a><span data-ttu-id="8eca2-103">Bookmark (evento)</span><span class="sxs-lookup"><span data-stu-id="8eca2-103">Bookmark Event</span></span>

<span data-ttu-id="8eca2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8eca2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8eca2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="8eca2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8eca2-106">Se produce cuando se activa un marcador en una cadena de texto de voz que ha definido la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8eca2-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="8eca2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="8eca2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8eca2-108">Marcador de **Sub** *Agent* \_  **(ByVal** \*BookmarkID \*\* \* *)*</span><span class="sxs-lookup"><span data-stu-id="8eca2-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="8eca2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8eca2-109">Part</span></span>         | <span data-ttu-id="8eca2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8eca2-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="8eca2-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="8eca2-111">*BookmarkID*</span></span> | <span data-ttu-id="8eca2-112">Entero largo que identifica el número de marcador.</span><span class="sxs-lookup"><span data-stu-id="8eca2-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8eca2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8eca2-113">Remarks</span></span>

<span data-ttu-id="8eca2-114">Para especificar un evento de marcador, use el método [**Speak**](speak-method.md) con una etiqueta **MRK** en el texto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="8eca2-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="8eca2-115">Para obtener más información acerca de las etiquetas, consulte etiquetas de salida de voz.</span><span class="sxs-lookup"><span data-stu-id="8eca2-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




