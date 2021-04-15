---
description: La edición enriquecida 3,0 admite el IME de HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante el uso de teclas de acceso rápido de una de estas dos maneras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547110"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="d2a52-103">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="d2a52-103">HexToUnicode IME</span></span>

<span data-ttu-id="d2a52-104">La edición enriquecida 3,0 admite el IME de HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante el uso de teclas de acceso rápido de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="d2a52-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="d2a52-105">Con el primer método de conversión, el usuario escribe el código de carácter en hexadecimal y, a continuación, presiona ALT + X.</span><span class="sxs-lookup"><span data-stu-id="d2a52-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="d2a52-106">El IME reemplaza los dígitos hexadecimales que preceden al punto de inserción con el carácter Unicode.</span><span class="sxs-lookup"><span data-stu-id="d2a52-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="d2a52-107">Si la fuente actual no admite el código de carácter, se elige una fuente adecuada que lo admita.</span><span class="sxs-lookup"><span data-stu-id="d2a52-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="d2a52-108">Para convertir de Unicode a hexadecimal, el usuario escribe MAYÚS + ALT + X.</span><span class="sxs-lookup"><span data-stu-id="d2a52-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="d2a52-109">Esta entrada reemplaza el carácter Unicode que precede al punto de inserción con los dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="d2a52-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="d2a52-110">En concreto, este método permite al usuario determinar el carácter que se indica mediante un indicador de "glifo que falta".</span><span class="sxs-lookup"><span data-stu-id="d2a52-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="d2a52-111">Si el código de carácter hexadecimal sigue inmediatamente a algunos caracteres hexadecimales legítimos (no de caracteres), el usuario selecciona los dígitos específicos que se van a convertir antes de escribir ALT + X.</span><span class="sxs-lookup"><span data-stu-id="d2a52-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="d2a52-112">Un problema con este primer método es que ALT + X se usa a veces como una combinación de teclas para el comando Exit (es decir, eXit).</span><span class="sxs-lookup"><span data-stu-id="d2a52-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="d2a52-113">Por ejemplo, en Microsoft Office, este comando solo aparece como una opción del menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="d2a52-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="d2a52-114">El segundo método de conversión entre caracteres hexadecimales y Unicode implica el panel numérico.</span><span class="sxs-lookup"><span data-stu-id="d2a52-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="d2a52-115">Con este método, el usuario escribe los números de ALT + teclado (con valores mayores que 255) para escribir caracteres Unicode mediante valores decimales.</span><span class="sxs-lookup"><span data-stu-id="d2a52-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="d2a52-116">Este método no es tan útil como el primero porque el usuario no puede ver qué dígitos hexadecimales se han escrito.</span><span class="sxs-lookup"><span data-stu-id="d2a52-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="d2a52-117">Además, el usuario no puede corregir los dígitos hexadecimales, excepto si vuelve a escribir todos los dígitos.</span><span class="sxs-lookup"><span data-stu-id="d2a52-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2a52-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2a52-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2a52-119">Acerca del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d2a52-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



