---
title: Etiqueta lst
description: Etiqueta lst
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532133"
---
# <a name="lst-tag"></a><span data-ttu-id="d5268-103">Etiqueta lst</span><span class="sxs-lookup"><span data-stu-id="d5268-103">Lst Tag</span></span>

<span data-ttu-id="d5268-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5268-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d5268-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="d5268-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d5268-106">Repite la última instrucción oral del carácter.</span><span class="sxs-lookup"><span data-stu-id="d5268-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="d5268-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="d5268-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d5268-108">\\**LST**</span><span class="sxs-lookup"><span data-stu-id="d5268-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="d5268-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5268-109">Remarks</span></span>

<span data-ttu-id="d5268-110">Esta etiqueta permite que un carácter repita su última instrucción oral.</span><span class="sxs-lookup"><span data-stu-id="d5268-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="d5268-111">Esta etiqueta debe aparecer por sí misma en el método [**Speak**](speak-method.md) ; no se puede incluir ningún otro texto o parámetro.</span><span class="sxs-lookup"><span data-stu-id="d5268-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="d5268-112">Cuando se repite el texto hablado, cualquier otra etiqueta incluida en el texto original se repite, excepto para los marcadores.</span><span class="sxs-lookup"><span data-stu-id="d5268-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="d5268-113">Cualquier. WAV y. Los archivos LWV incluidos en el texto también se repiten.</span><span class="sxs-lookup"><span data-stu-id="d5268-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




