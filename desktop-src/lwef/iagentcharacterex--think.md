---
title: IAgentCharacterEx creer
description: IAgentCharacterEx creer
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077656"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="001c5-103">IAgentCharacterEx:: cree</span><span class="sxs-lookup"><span data-stu-id="001c5-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="001c5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="001c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="001c5-105">Muestra el globo de palabra pensamiento del carácter con el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="001c5-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="001c5-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="001c5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="001c5-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="001c5-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="001c5-108">Texto que se va a mostrar en el globo de pensamiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="001c5-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="001c5-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="001c5-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="001c5-110">Dirección de una variable que recibe el identificador de solicitud de **reflexión** .</span><span class="sxs-lookup"><span data-stu-id="001c5-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="001c5-111">Al igual que el método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , el método de **reflexión** es una solicitud en cola que muestra texto en un globo de palabras, con la excepción de que las ideas se muestran en un globo de pensamiento especial.</span><span class="sxs-lookup"><span data-stu-id="001c5-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="001c5-112">El globo de pensamiento solo admite la etiqueta de control de voz de marcador (**\\ MRK**) y omite cualquier otra etiqueta de control de voz.</span><span class="sxs-lookup"><span data-stu-id="001c5-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="001c5-113">A diferencia de **IAgentCharacter:: Speak**, el método de **reflexión** no cambia el estado de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="001c5-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="001c5-114">La configuración de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) también se aplica al estilo de apariencia del globo de pensamiento.</span><span class="sxs-lookup"><span data-stu-id="001c5-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="001c5-115">Por ejemplo, la propiedad [**Enabled**](enabled-property.md) del globo también debe ser **true** para que el texto se muestre.</span><span class="sxs-lookup"><span data-stu-id="001c5-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="001c5-116">La separación de palabras automática del agente de Microsoft en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio y tabulación).</span><span class="sxs-lookup"><span data-stu-id="001c5-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="001c5-117">Sin embargo, puede dividir una palabra en el globo también.</span><span class="sxs-lookup"><span data-stu-id="001c5-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="001c5-118">En idiomas como el japonés, el chino y el tailandés, donde no se usan espacios para romper palabras, inserte un carácter de espacio de ancho cero de Unicode (0x200B) entre los caracteres para definir los saltos de palabra lógicos.</span><span class="sxs-lookup"><span data-stu-id="001c5-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="001c5-119">Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) para garantizar la presentación de texto adecuada en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="001c5-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="001c5-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="001c5-120">See Also</span></span>

<span data-ttu-id="001c5-121">[**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: setStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="001c5-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 