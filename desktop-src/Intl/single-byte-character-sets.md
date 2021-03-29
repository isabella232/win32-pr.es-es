---
description: Un juego de caracteres de un solo byte (SBCS) es una asignación de 256 caracteres individuales a sus valores de código de identificación, que se implementa como una página de códigos.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Juegos de caracteres de un solo byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003055"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="a64eb-103">Juegos de caracteres de un solo byte</span><span class="sxs-lookup"><span data-stu-id="a64eb-103">Single-byte Character Sets</span></span>

<span data-ttu-id="a64eb-104">Un juego de caracteres de un solo byte (SBCS) es una asignación de 256 caracteres individuales a sus valores de código de identificación, que se implementa como una página de códigos.</span><span class="sxs-lookup"><span data-stu-id="a64eb-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="a64eb-105">SBCS puede corresponder a una página de códigos de Windows o a una página de códigos OEM.</span><span class="sxs-lookup"><span data-stu-id="a64eb-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="a64eb-106">Una página de códigos SBCS también puede incluir una página de códigos no nativa, por ejemplo, una página de códigos EBCDIC.</span><span class="sxs-lookup"><span data-stu-id="a64eb-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="a64eb-107">Para ver las definiciones de estas páginas de códigos, vea [páginas de códigos](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="a64eb-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="a64eb-108">Las nuevas aplicaciones de Windows deben usar [Unicode](unicode.md) para evitar las incoherencias de las distintas páginas de códigos y para facilitar la localización.</span><span class="sxs-lookup"><span data-stu-id="a64eb-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="a64eb-109">Sin embargo, algunos protocolos heredados requieren el uso de SBCS.</span><span class="sxs-lookup"><span data-stu-id="a64eb-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="a64eb-110">Cada página de códigos SBCS admite distintos caracteres, pero ninguna página admite toda la amplitud de caracteres proporcionados por Unicode.</span><span class="sxs-lookup"><span data-stu-id="a64eb-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="a64eb-111">Cada página de códigos SBCS admite un subconjunto diferente, codificado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="a64eb-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="a64eb-112">Los datos convertidos de una página de códigos SBCS a otra están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente.</span><span class="sxs-lookup"><span data-stu-id="a64eb-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="a64eb-113">Los datos convertidos de Unicode a SBCS están sujetos a la pérdida de datos porque es posible que una página de códigos determinada no pueda representar todos los caracteres utilizados en esos datos Unicode concretos.</span><span class="sxs-lookup"><span data-stu-id="a64eb-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="a64eb-114">Las aplicaciones usan páginas de códigos de Windows SBCS con las versiones "A" de las funciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="a64eb-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="a64eb-115">Vea [convenciones para prototipos de función](conventions-for-function-prototypes.md) y [páginas de códigos](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="a64eb-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="a64eb-116">Para ayudar a identificar una página de códigos SBCS, una aplicación puede usar la función [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a64eb-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="a64eb-117">Además, una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para asignar entre cadenas Unicode y SBCS.</span><span class="sxs-lookup"><span data-stu-id="a64eb-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a64eb-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a64eb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64eb-119">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="a64eb-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="a64eb-120">Juegos de caracteres de doble byte</span><span class="sxs-lookup"><span data-stu-id="a64eb-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



