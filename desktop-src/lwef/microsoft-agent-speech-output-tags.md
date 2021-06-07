---
title: Etiquetas de salida de voz de Microsoft Agent
description: Etiquetas de salida de voz de Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386804"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="f3e4f-103">Etiquetas de salida de voz de Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="f3e4f-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="f3e4f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3e4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f3e4f-105">Los servicios de Microsoft Agent admiten la modificación de la salida de voz a través de etiquetas especiales insertadas en la cadena de texto de voz.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="f3e4f-106">Estas etiquetas le ayudan a cambiar las características de la expresión de salida del carácter.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="f3e4f-107">Las etiquetas de salida de voz usan las siguientes reglas de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="f3e4f-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="f3e4f-108">Todas las etiquetas comienzan y terminan con un carácter de barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f3e4f-108">All tags begin and end with a backslash character (\\).</span></span>
-   <span data-ttu-id="f3e4f-109">El carácter de barra diagonal inversa única no está habilitado dentro de una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="f3e4f-110">Para incluir un carácter de barra diagonal inversa en un parámetro de texto de una etiqueta, use una doble barra diagonal inversa ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="f3e4f-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\\).</span></span>
-   <span data-ttu-id="f3e4f-111">Las etiquetas no tienen en cuenta mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-111">Tags are case-insensitive.</span></span> <span data-ttu-id="f3e4f-112">Por ejemplo, \\ pit es igual que \\ \\ \\ PIT.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="f3e4f-113">Las etiquetas dependen del espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="f3e4f-114">Por ejemplo, \\ Rst \\ no es igual que \\ \\ Rst.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="f3e4f-115">A menos que otra etiqueta especifique o modifique de otro modo, la salida de voz conserva la característica establecida por la etiqueta dentro del texto especificado en un único [**método Speak.**](speak-method.md)</span><span class="sxs-lookup"><span data-stu-id="f3e4f-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="f3e4f-116">La salida de voz se restablece automáticamente a través de los parámetros definidos por el usuario una vez completado un **método Speak.**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="f3e4f-117">Algunas etiquetas incluyen cadenas entre comillas.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-117">Some tags include quoted strings.</span></span> <span data-ttu-id="f3e4f-118">Para algunos lenguajes de programación, como Visual Basic Scripting Edition (VBScript) y Visual Basic, esto significa que puede que tenga que usar dos comillas para designar el parámetro de la etiqueta o concatenar un carácter de comillas dobles como parte de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="f3e4f-119">Este último se muestra en este Visual Basic ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3e4f-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="f3e4f-120">Para C, C++ y Java™ programación, preceda las barras diagonales inversas y las comillas dobles con una barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="f3e4f-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3e4f-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="f3e4f-122">Para los idiomas externos que admiten caracteres de juego de caracteres de doble byte (DBCS), puede usar caracteres de doble byte para especificar parámetros de cadena.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="f3e4f-123">Sin embargo, use caracteres de un solo byte para todos los demás parámetros y caracteres que se usan para definir la etiqueta, incluida la propia etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="f3e4f-124">Se admiten las siguientes etiquetas:</span><span class="sxs-lookup"><span data-stu-id="f3e4f-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="f3e4f-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="f3e4f-126">**Ctx**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="f3e4f-127">**Emp**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="f3e4f-128">**Lst**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="f3e4f-129">**Asignación**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="f3e4f-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="f3e4f-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="f3e4f-132">**Hoyo**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="f3e4f-133">**Rst**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="f3e4f-134">**Spd**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="f3e4f-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="f3e4f-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="f3e4f-136">Las etiquetas están diseñadas principalmente para ajustar la salida generada por texto a voz (TTS).</span><span class="sxs-lookup"><span data-stu-id="f3e4f-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="f3e4f-137">Solo se pueden usar las etiquetas [**Mrk**](mrk-tag.md) y [**Map**](map-tag.md) con salida hablada basada en archivos de sonido.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="f3e4f-138">Microsoft Agent no admite todas las etiquetas documentadas en el SDK de Voz de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="f3e4f-139">Los parámetros también pueden variar en función del motor de TTS seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f3e4f-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="f3e4f-140">Puede establecer un motor de TTS específico mediante [**TTSModeID.**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="f3e4f-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




