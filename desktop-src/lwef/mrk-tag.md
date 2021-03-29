---
title: Etiqueta MRK
description: Etiqueta MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776045"
---
# <a name="mrk-tag"></a><span data-ttu-id="f6dbe-103">Etiqueta MRK</span><span class="sxs-lookup"><span data-stu-id="f6dbe-103">Mrk Tag</span></span>

<span data-ttu-id="f6dbe-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6dbe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f6dbe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="f6dbe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f6dbe-106">Define un marcador en el texto hablado.</span><span class="sxs-lookup"><span data-stu-id="f6dbe-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="f6dbe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="f6dbe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f6dbe-108">**\\MRK =***número***\\**</span><span class="sxs-lookup"><span data-stu-id="f6dbe-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="f6dbe-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f6dbe-109">Part</span></span>     | <span data-ttu-id="f6dbe-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6dbe-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="f6dbe-111">*número*</span><span class="sxs-lookup"><span data-stu-id="f6dbe-111">*number*</span></span> | <span data-ttu-id="f6dbe-112">Valor entero largo que identifica el marcador.</span><span class="sxs-lookup"><span data-stu-id="f6dbe-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f6dbe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6dbe-113">Remarks</span></span>

<span data-ttu-id="f6dbe-114">Cuando el servidor procesa un marcador, genera un evento de marcador.</span><span class="sxs-lookup"><span data-stu-id="f6dbe-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="f6dbe-115">Debe especificar un número mayor que cero (0) y distinto de 2147483647 o 2147483646.</span><span class="sxs-lookup"><span data-stu-id="f6dbe-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




