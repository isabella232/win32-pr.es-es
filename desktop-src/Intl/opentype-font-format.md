---
description: El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fuente OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653065"
---
# <a name="opentype-font-format"></a><span data-ttu-id="1a785-103">Formato de fuente OpenType</span><span class="sxs-lookup"><span data-stu-id="1a785-103">OpenType Font Format</span></span>

<span data-ttu-id="1a785-104">El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1a785-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="1a785-105">Las fuentes OpenType permiten la asignación entre caracteres y [glifos](uniscribe-glossary.md), habilitando la compatibilidad con ligaduras, formatos posicionales, alternativas y otras sustituciones.</span><span class="sxs-lookup"><span data-stu-id="1a785-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="1a785-106">Las fuentes OpenType también pueden incluir información que admite la posición de glifos bidimensionales y los datos adjuntos del glifo, y pueden contener contornos TrueType o PostScript.</span><span class="sxs-lookup"><span data-stu-id="1a785-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="1a785-107">Las características de diseño dentro de las fuentes OpenType se organizan por scripts y lenguajes, lo que permite que una sola fuente admita varios sistemas de escritura, incluso dentro del mismo script.</span><span class="sxs-lookup"><span data-stu-id="1a785-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="1a785-108">Para garantizar la coherencia en las operaciones de diseño de texto y evitar una sobrecarga innecesaria en archivos o aplicaciones de fuentes, muchos de los algoritmos de diseño de texto y semánticos del lenguaje se incluyen en Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="1a785-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="1a785-109">Esto evita que el desarrollador de fuentes tenga que definir reglas de script generalizadas dentro de una fuente.</span><span class="sxs-lookup"><span data-stu-id="1a785-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="1a785-110">Las aplicaciones pueden introducir información o preferencias específicas en relación con el diseño del script.</span><span class="sxs-lookup"><span data-stu-id="1a785-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="1a785-111">Las fuentes de diseño OpenType pueden incluir incluso reglas de diseño que dupliquen o reemplacen a las aplicadas por los servicios del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a785-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="1a785-112">La estructura en capas de los servicios del sistema operativo que admiten el diseño de texto permite a una aplicación elegir la información de diseño que se va a utilizar y seleccionar cómo aplicarla.</span><span class="sxs-lookup"><span data-stu-id="1a785-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="1a785-113">Para obtener más información, vea información [General sobre las especificaciones tipográficas de Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la [especificación OpenType](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="1a785-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a785-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a785-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a785-115">Acerca de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="1a785-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



