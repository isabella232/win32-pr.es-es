---
title: Propiedad Enabled (objeto AudioOutput)
description: Obtenga información sobre la propiedad de objeto AudioOutput habilitada. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407348"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="45af8-104">Propiedad Enabled (objeto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="45af8-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="45af8-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45af8-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="45af8-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45af8-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="45af8-107">Devuelve un valor booleano que indica si la salida de audio (hablada) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="45af8-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="45af8-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="45af8-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="45af8-109">*agent!". AudioOutput.Enabled*\*</span><span class="sxs-lookup"><span data-stu-id="45af8-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="45af8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="45af8-110">Value</span></span>     | <span data-ttu-id="45af8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="45af8-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="45af8-112">**True**</span><span class="sxs-lookup"><span data-stu-id="45af8-112">**True**</span></span>  | <span data-ttu-id="45af8-113">(Valor predeterminado) La salida de audio hablado está habilitada.</span><span class="sxs-lookup"><span data-stu-id="45af8-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="45af8-114">**False**</span><span class="sxs-lookup"><span data-stu-id="45af8-114">**False**</span></span> | <span data-ttu-id="45af8-115">La salida de audio hablado está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="45af8-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45af8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45af8-116">Remarks</span></span>

<span data-ttu-id="45af8-117">Esta propiedad refleja la opción Reproducir salida de audio en la página Salida de la hoja de propiedades agente (Opciones avanzadas de caracteres).</span><span class="sxs-lookup"><span data-stu-id="45af8-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="45af8-118">Cuando la [**propiedad Enabled**](enabled-property.md) devuelve **True**, el método [**Speak**](speak-method.md) genera una salida de audio si está instalado un motor TTS compatible o usa archivos de sonido para la salida hablada.</span><span class="sxs-lookup"><span data-stu-id="45af8-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="45af8-119">Cuando devuelve **False**, significa que la salida de voz no está instalada o el usuario la ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="45af8-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="45af8-120">La configuración de propiedad se aplica a todos los caracteres del Agente y es de solo lectura; solo el usuario puede establecer este valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="45af8-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="45af8-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45af8-121">See Also</span></span>

[<span data-ttu-id="45af8-122">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="45af8-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




