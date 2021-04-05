---
title: Propiedad Enabled (objeto AudioOutput)
description: Propiedad Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078770"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="a97bd-103">Propiedad Enabled (objeto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="a97bd-103">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="a97bd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a97bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a97bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="a97bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a97bd-106">Devuelve un valor booleano que indica si está habilitada la salida de audio (hablado).</span><span class="sxs-lookup"><span data-stu-id="a97bd-106">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a97bd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="a97bd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a97bd-108">*agente \* \* *. AudioOutput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="a97bd-108">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="a97bd-109">Value</span><span class="sxs-lookup"><span data-stu-id="a97bd-109">Value</span></span>     | <span data-ttu-id="a97bd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a97bd-110">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="a97bd-111">**True**</span><span class="sxs-lookup"><span data-stu-id="a97bd-111">**True**</span></span>  | <span data-ttu-id="a97bd-112">Predeterminada La salida de audio oral está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a97bd-112">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="a97bd-113">**False**</span><span class="sxs-lookup"><span data-stu-id="a97bd-113">**False**</span></span> | <span data-ttu-id="a97bd-114">La salida de audio hablada está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="a97bd-114">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a97bd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a97bd-115">Remarks</span></span>

<span data-ttu-id="a97bd-116">Esta propiedad refleja la opción reproducir salida de audio en la página salida de la hoja de propiedades del agente (opciones avanzadas de caracteres).</span><span class="sxs-lookup"><span data-stu-id="a97bd-116">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="a97bd-117">Cuando la propiedad [**Enabled**](enabled-property.md) devuelve **true**, el método [**Speak**](speak-method.md) genera una salida de audio si se instala un motor TTS compatible o si se usan archivos de sonido para la salida de voz.</span><span class="sxs-lookup"><span data-stu-id="a97bd-117">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="a97bd-118">Cuando devuelve **false**, significa que la salida de voz no está instalada o que el usuario ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a97bd-118">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="a97bd-119">La configuración de la propiedad se aplica a todos los caracteres del agente y es de solo lectura; solo el usuario puede establecer este valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a97bd-119">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="a97bd-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a97bd-120">See Also</span></span>

[<span data-ttu-id="a97bd-121">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="a97bd-121">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




