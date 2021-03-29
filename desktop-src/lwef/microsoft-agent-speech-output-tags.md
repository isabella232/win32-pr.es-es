---
title: Etiquetas de salida de voz del agente de Microsoft
description: Etiquetas de salida de voz del agente de Microsoft
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903508"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="e0e2c-103">Etiquetas de salida de voz del agente de Microsoft</span><span class="sxs-lookup"><span data-stu-id="e0e2c-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="e0e2c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0e2c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e0e2c-105">Los servicios del agente de Microsoft admiten la modificación de la salida de voz a través de etiquetas especiales insertadas en la cadena de texto de voz.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="e0e2c-106">Estas etiquetas le ayudan a cambiar las características de la expresión de salida del carácter.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="e0e2c-107">Las etiquetas de salida de voz usan las siguientes reglas de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e0e2c-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="e0e2c-108">Todas las etiquetas comienzan y terminan con un carácter de barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="e0e2c-109">El carácter de barra diagonal inversa única no está habilitado dentro de una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="e0e2c-110">Para incluir un carácter de barra diagonal inversa en un parámetro de texto de una etiqueta, utilice una doble barra diagonal inversa ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="e0e2c-111">Las etiquetas no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-111">Tags are case-insensitive.</span></span> <span data-ttu-id="e0e2c-112">Por ejemplo, \\ Pit \\ es igual que \\ Pit \\ .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="e0e2c-113">Las etiquetas dependen del espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="e0e2c-114">Por ejemplo, \\ RST \\ no es lo mismo que \\ RST \\ .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="e0e2c-115">A menos que otra etiqueta especifique o modifique de otro modo, la salida de voz conservará la característica establecida por la etiqueta en el texto especificado en un solo método [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="e0e2c-116">La salida de voz se restablece automáticamente a través de los parámetros definidos por el usuario una vez completado un método **Speak** .</span><span class="sxs-lookup"><span data-stu-id="e0e2c-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="e0e2c-117">Algunas etiquetas incluyen cadenas entre comillas.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-117">Some tags include quoted strings.</span></span> <span data-ttu-id="e0e2c-118">En algunos lenguajes de programación, como Visual Basic Scripting Edition (VBScript) y Visual Basic, esto significa que puede que tenga que utilizar dos comillas para designar el parámetro de la etiqueta o concatenar un carácter de comilla doble como parte de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="e0e2c-119">Este último se muestra en este Visual Basic ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0e2c-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="e0e2c-120">Para C, C++ y Java™ programación, preceden a las barras diagonales inversas y comillas dobles con una barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="e0e2c-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0e2c-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="e0e2c-122">En el caso de los idiomas externos que admiten caracteres de juegos de caracteres de doble byte (DBCS), puede usar caracteres de doble byte para especificar parámetros de cadena.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="e0e2c-123">Sin embargo, use caracteres de un solo byte para todos los demás parámetros y caracteres que se usan para definir la etiqueta, incluida la propia etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="e0e2c-124">Se admiten las siguientes etiquetas:</span><span class="sxs-lookup"><span data-stu-id="e0e2c-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="e0e2c-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="e0e2c-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="e0e2c-127">**Empleado**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="e0e2c-128">**LST**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="e0e2c-129">**Conectarse**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="e0e2c-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="e0e2c-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="e0e2c-132">**Pozo**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="e0e2c-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="e0e2c-134">**DOCUP**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="e0e2c-135">**Volumen**</span><span class="sxs-lookup"><span data-stu-id="e0e2c-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="e0e2c-136">Las etiquetas están diseñadas principalmente para ajustar los resultados generados por texto a voz (TTS).</span><span class="sxs-lookup"><span data-stu-id="e0e2c-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="e0e2c-137">Solo se pueden usar las etiquetas [**MRK**](mrk-tag.md) y [**map**](map-tag.md) con la salida de voz basada en archivos de sonido.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="e0e2c-138">El agente de Microsoft no admite todas las etiquetas documentadas en el SDK de Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="e0e2c-139">Los parámetros también pueden variar en función del motor TTS seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e0e2c-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="e0e2c-140">Puede establecer un motor TTS específico mediante [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="e0e2c-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




