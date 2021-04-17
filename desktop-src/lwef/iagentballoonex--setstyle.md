---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704815"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="13f4c-103">IAgentBalloonEx:: SetStyle</span><span class="sxs-lookup"><span data-stu-id="13f4c-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="13f4c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13f4c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="13f4c-105">Recupera la configuración de estilo de globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="13f4c-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="13f4c-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="13f4c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="13f4c-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span><span class="sxs-lookup"><span data-stu-id="13f4c-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="13f4c-108">Configuración de estilo para el globo de palabras, que puede ser una combinación de cualquiera de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="13f4c-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="13f4c-109">Value</span><span class="sxs-lookup"><span data-stu-id="13f4c-109">Value</span></span>                                                                            | <span data-ttu-id="13f4c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="13f4c-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="13f4c-111">constante de estilo de globo **corto sin signo de const** **\_ \_ = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="13f4c-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="13f4c-112">El globo es compatible con la salida.</span><span class="sxs-lookup"><span data-stu-id="13f4c-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="13f4c-113">**const unsigned short** **Balloon \_ style \_ SIZETOTEXT = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="13f4c-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="13f4c-114">El alto del globo tiene el tamaño adecuado para la salida de texto.</span><span class="sxs-lookup"><span data-stu-id="13f4c-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="13f4c-115">tipo de globo **corto sin signo const** **\_ \_ Ocultar automáticamente = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="13f4c-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="13f4c-116">El globo se oculta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="13f4c-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="13f4c-117">tipo de globo **corto sin signo const** **\_ \_ autopace = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="13f4c-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="13f4c-118">La salida de texto se acelera según la tasa de salida.</span><span class="sxs-lookup"><span data-stu-id="13f4c-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="13f4c-119">Cuando se establece el bit de estilo de **globoon** , el globo de palabras aparece cuando se usa el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) , a menos que el usuario invalide su presentación en la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13f4c-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="13f4c-120">Cuando no se establece, no aparece ningún globo.</span><span class="sxs-lookup"><span data-stu-id="13f4c-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="13f4c-121">Cuando se establece el bit de estilo **SizeToText** , el globo de palabras ajusta automáticamente el alto del globo al tamaño actual del texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="13f4c-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="13f4c-122">Cuando no se establece, el alto del globo se basa en el valor de la propiedad número de líneas del globo.</span><span class="sxs-lookup"><span data-stu-id="13f4c-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="13f4c-123">Este bit de estilo se establece en 1 y un intento de usar [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) producirá un error.</span><span class="sxs-lookup"><span data-stu-id="13f4c-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="13f4c-124">Cuando se establece el bit de estilo de **ocultación** automática, el globo de palabras se oculta automáticamente tras un breve tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="13f4c-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="13f4c-125">Cuando no se establece, el globo se muestra hasta una nueva llamada de [**voz**](speak-method.md) o de [**reflexión**](think-method.md) , el carácter está oculto o el usuario hace clic o arrastra el carácter.</span><span class="sxs-lookup"><span data-stu-id="13f4c-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="13f4c-126">Cuando se establece el bit de estilo **autopace** , el globo de palabras acelera la salida en función de la tasa de salida actual, por ejemplo, una palabra a la vez.</span><span class="sxs-lookup"><span data-stu-id="13f4c-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="13f4c-127">Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="13f4c-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="13f4c-128">Cuando no se establece, todo el texto incluido en una instrucción [**Speak**](speak-method.md) o de [**reflexión**](think-method.md) se muestra a la vez.</span><span class="sxs-lookup"><span data-stu-id="13f4c-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="13f4c-129">La propiedad de estilo del globo se puede establecer incluso si el usuario ha deshabilitado la presentación del globo mediante la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="13f4c-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="13f4c-130">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="13f4c-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="13f4c-131">Los valores predeterminados para estos bits de estilo se basan en su configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13f4c-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="13f4c-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13f4c-132">See Also</span></span>

[<span data-ttu-id="13f4c-133">**IAgentBalloonEx:: GetStyle**</span><span class="sxs-lookup"><span data-stu-id="13f4c-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





