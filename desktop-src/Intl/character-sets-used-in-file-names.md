---
description: NTFS almacena los nombres de archivo en Unicode. En cambio, los sistemas de archivos FAT12, FAT16 y FAT32 antiguos utilizan el juego de caracteres OEM. Para obtener más información, vea Páginas de códigos.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Juegos de caracteres usados en nombres de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910722"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="9746e-105">Juegos de caracteres usados en nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="9746e-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="9746e-106">NTFS almacena los nombres de archivo en Unicode.</span><span class="sxs-lookup"><span data-stu-id="9746e-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="9746e-107">En cambio, los sistemas de archivos FAT12, FAT16 y FAT32 antiguos utilizan el juego de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="9746e-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="9746e-108">Para obtener más información, vea [Páginas de códigos](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="9746e-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="9746e-109">A veces, las aplicaciones no Unicode que crean archivos FAT tienen que usar las funciones de conversión de la biblioteca en tiempo de ejecución estándar de C para traducir entre el juego de caracteres de la página de códigos de Windows y el juego de caracteres de página de códigos OEM.</span><span class="sxs-lookup"><span data-stu-id="9746e-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="9746e-110">Con las implementaciones Unicode de las funciones del sistema de archivos, no es necesario realizar dichas traducciones.</span><span class="sxs-lookup"><span data-stu-id="9746e-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="9746e-111">La aplicación puede usar tipos de cadena genéricos, como se describe en [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="9746e-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="9746e-112">La aplicación también puede utilizar prototipos de función genéricos mediante técnicas descritas en [convenciones para prototipos de función](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="9746e-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="9746e-113">En el caso de tipos de cadena genéricos o prototipos de función genéricos, la aplicación puede usar un solo archivo de código fuente para compilar una versión de Unicode o no Unicode.</span><span class="sxs-lookup"><span data-stu-id="9746e-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="9746e-114">Para ello, la aplicación proporciona macros para las funciones que no se invocan al compilar para Unicode.</span><span class="sxs-lookup"><span data-stu-id="9746e-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="9746e-115">En los sistemas de archivos NTFS y FAT, los caracteres de nombre de archivo especiales son: ' \\ ', '/', '. ', '? ' y ' \* '.</span><span class="sxs-lookup"><span data-stu-id="9746e-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="9746e-116">En las páginas de códigos OEM, estos caracteres especiales están en el intervalo ASCII de caracteres (de 0x00 a 0x7F).</span><span class="sxs-lookup"><span data-stu-id="9746e-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="9746e-117">Sus equivalentes de Unicode son los mismos valores en un formato de 2 bytes, 0x0000 a 0x007F.</span><span class="sxs-lookup"><span data-stu-id="9746e-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="9746e-118">Los juegos de caracteres de página de códigos de Windows y de página de códigos OEM utilizados en los sistemas operativos en idioma japonés contienen el símbolo del yen (¥) en lugar de una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9746e-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="9746e-119">Por lo tanto, el símbolo del yen es un carácter prohibido para los sistemas de archivos NTFS y FAT.</span><span class="sxs-lookup"><span data-stu-id="9746e-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="9746e-120">Al asignar Unicode a una página de códigos en idioma japonés, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) y otras funciones de conversión asignan la barra diagonal inversa (u + 005C) y el símbolo de yen Unicode normal (u + 00A5) a este mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="9746e-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="9746e-121">Por motivos de seguridad, las aplicaciones no suelen permitir el carácter U + 00A5 en una cadena Unicode que podría convertirse para su uso como nombre de archivo FAT.</span><span class="sxs-lookup"><span data-stu-id="9746e-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="9746e-122">Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="9746e-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9746e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9746e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9746e-124">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="9746e-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="9746e-125">Consideraciones de seguridad: características internacionales</span><span class="sxs-lookup"><span data-stu-id="9746e-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



