---
title: Etiqueta CTX
description: Etiqueta CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075962"
---
# <a name="ctx-tag"></a><span data-ttu-id="54f49-103">Etiqueta CTX</span><span class="sxs-lookup"><span data-stu-id="54f49-103">Ctx Tag</span></span>

<span data-ttu-id="54f49-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54f49-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="54f49-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="54f49-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="54f49-106">Establece el contexto del texto de salida.</span><span class="sxs-lookup"><span data-stu-id="54f49-106">Sets the context of the output text.</span></span>

</dd> <dt>

<span data-ttu-id="54f49-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="54f49-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="54f49-108">\\**CTX** = *cadena*</span><span class="sxs-lookup"><span data-stu-id="54f49-108">\\**Ctx**=*string*</span></span>\\



| <span data-ttu-id="54f49-109">Parte</span><span class="sxs-lookup"><span data-stu-id="54f49-109">Part</span></span>     | <span data-ttu-id="54f49-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f49-110">Description</span></span>                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f49-111">*string*</span><span class="sxs-lookup"><span data-stu-id="54f49-111">*string*</span></span> | <span data-ttu-id="54f49-112">Cadena que especifica el contexto del texto que se muestra a continuación, que determina cómo se pronuncian los símbolos o las abreviaturas.</span><span class="sxs-lookup"><span data-stu-id="54f49-112">A string specifying the context of the text that follows, which determines how symbols or abbreviations are spoken.</span></span><br/> <span data-ttu-id="54f49-113">**"Dirección"**    Direcciones o números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="54f49-113">**"Address"**    Addresses and/or phone numbers.</span></span><br/> <span data-ttu-id="54f49-114">**"Correo electrónico"**    Correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="54f49-114">**"E-mail"**    Electronic mail.</span></span><br/> <span data-ttu-id="54f49-115">Se desconoce el contexto **"desconocido"** (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="54f49-115">**"Unknown"**    (Default) Context is unknown.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="54f49-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54f49-116">Remarks</span></span>

<span data-ttu-id="54f49-117">Esta etiqueta solo se admite para la salida generada por TTS.</span><span class="sxs-lookup"><span data-stu-id="54f49-117">This tag is supported only for TTS-generated output.</span></span> <span data-ttu-id="54f49-118">El intervalo de valores para el parámetro puede variar en función del motor TTS instalado.</span><span class="sxs-lookup"><span data-stu-id="54f49-118">The range of values for the parameter may vary depending on the installed TTS engine.</span></span>

 

 





