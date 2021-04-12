---
title: Propiedad de estilo
description: Propiedad de estilo
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357121"
---
# <a name="style-property"></a><span data-ttu-id="27b18-103">Propiedad de estilo</span><span class="sxs-lookup"><span data-stu-id="27b18-103">Style Property</span></span>

<span data-ttu-id="27b18-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27b18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="27b18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="27b18-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="27b18-106">Devuelve o establece el estilo de salida de globo de palabra del carácter.</span><span class="sxs-lookup"><span data-stu-id="27b18-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="27b18-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="27b18-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="27b18-108">\*agente. ***Caracteres ("*** CharacterID \* *"). Estilo de globo. Style* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="27b18-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="27b18-109">Parte</span><span class="sxs-lookup"><span data-stu-id="27b18-109">Part</span></span>    | <span data-ttu-id="27b18-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="27b18-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b18-111">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="27b18-111">*Style*</span></span> | <span data-ttu-id="27b18-112">Entero que representa el estilo de salida del globo.</span><span class="sxs-lookup"><span data-stu-id="27b18-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="27b18-113">La configuración de estilo es un campo de bits con bits que corresponden a: globo-sobre (bit 0), tamaño a texto (bit 1), ocultación automática (bit 2), velocidad automática (bit 3), número de caracteres por línea (bits 16-23) y número de líneas (bits 24-31).</span><span class="sxs-lookup"><span data-stu-id="27b18-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27b18-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27b18-114">Remarks</span></span>

<span data-ttu-id="27b18-115">Cuando el bit de estilo de globo está establecido en 1, el globo de palabras aparece cuando se [**usa un método**](https://www.bing.com/search?q=**Speak**) de lectura o de [**reflexión**](think-method.md) , a menos que el usuario Invalide este valor en la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27b18-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="27b18-116">Cuando se establece en 0, no aparece un globo.</span><span class="sxs-lookup"><span data-stu-id="27b18-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="27b18-117">Cuando el bit de estilo de tamaño a texto se establece en 1, el globo de palabras ajusta automáticamente el alto del globo al tamaño actual del texto para la [**instrucción de lectura o de**](https://www.bing.com/search?q=**Speak**) [**reflexión**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="27b18-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="27b18-118">Cuando se establece en 0, el alto del globo se basa en el valor de la propiedad [**NumberOfLines**](numberoflines-property.md) .</span><span class="sxs-lookup"><span data-stu-id="27b18-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="27b18-119">Si este bit de estilo se establece en 1 y se intenta establecer la propiedad **NumberOfLines** , el agente genera un error.</span><span class="sxs-lookup"><span data-stu-id="27b18-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="27b18-120">Cuando el bit de estilo de ocultación automática está establecido en 1, el globo de palabras se oculta automáticamente cuando se completa la salida de voz.</span><span class="sxs-lookup"><span data-stu-id="27b18-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="27b18-121">Cuando se establece en 0, el globo sigue mostrándose hasta la siguiente llamada de [**hablar**](https://www.bing.com/search?q=**Speak**) o [**pensar**](think-method.md) , el carácter está oculto o el usuario hace clic en el carácter o lo arrastra.</span><span class="sxs-lookup"><span data-stu-id="27b18-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="27b18-122">Cuando el bit de estilo auto-Pace está establecido en 1, el globo de palabras acelera la salida en función de la tasa de salida actual, por ejemplo, una palabra a la vez.</span><span class="sxs-lookup"><span data-stu-id="27b18-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="27b18-123">Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="27b18-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="27b18-124">Cuando se establece en 0, todo el texto incluido en una instrucción [**Speak**](https://www.bing.com/search?q=**Speak**) o de [**reflexión**](think-method.md) se muestra a la vez.</span><span class="sxs-lookup"><span data-stu-id="27b18-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="27b18-125">Para recuperar solo el valor de los cuatro bits inferiores **y** el valor devuelto por el **estilo** con 255.</span><span class="sxs-lookup"><span data-stu-id="27b18-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="27b18-126">Para establecer un valor de bit **o** el valor devuelto con el valor de los bits que desea establecer.</span><span class="sxs-lookup"><span data-stu-id="27b18-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="27b18-127">Para desactivar un bit **y** el valor devuelto con uno de los complementos del bit:</span><span class="sxs-lookup"><span data-stu-id="27b18-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="27b18-128">La propiedad de **estilo** también devuelve el número de caracteres por línea en el byte inferior de la palabra superior y el número de líneas en el byte alto de la palabra superior.</span><span class="sxs-lookup"><span data-stu-id="27b18-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="27b18-129">Aunque esto se puede leer más fácilmente mediante las propiedades [**CharsPerLine**](charsperline-property.md) y [**NumberOfLines**](numberoflines-property.md), la propiedad **Style** también permite establecer esos valores.</span><span class="sxs-lookup"><span data-stu-id="27b18-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="27b18-130">Por ejemplo, para cambiar el número de líneas, desactive los bits 24 a 31 con una operación **and** lógica antes de establecer el nuevo valor como el producto del nuevo valor las horas 2 ^ 24, agregados al valor existente de la propiedad **Style** .</span><span class="sxs-lookup"><span data-stu-id="27b18-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="27b18-131">Para establecer el número de caracteres por línea, desactive los bits 16 a 23 con una operación **and** lógica antes de establecer el nuevo valor como el producto del nuevo valor las veces 2 ^ 16, agregados al valor existente de la propiedad Style.</span><span class="sxs-lookup"><span data-stu-id="27b18-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="27b18-132">La propiedad de **estilo** se puede establecer incluso si el usuario ha deshabilitado la presentación de globos mediante la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="27b18-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="27b18-133">Sin embargo, los valores para el número de líneas deben estar entre 1 y 128 y el número de caracteres por línea debe estar entre 8 y 255.</span><span class="sxs-lookup"><span data-stu-id="27b18-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="27b18-134">Si proporciona un valor no válido para la propiedad **Style** , el agente producirá un error.</span><span class="sxs-lookup"><span data-stu-id="27b18-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="27b18-135">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="27b18-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="27b18-136">Los valores predeterminados para estos bits de estilo se basan en su configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27b18-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




