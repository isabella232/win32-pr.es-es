---
description: Las aplicaciones deben usar el carácter separador de línea (0x2028) y el carácter separador de párrafo (0x2029) para dividir el texto sin formato. Se inicia una nueva línea después de cada separador de línea. Se inicia un nuevo párrafo detrás de cada separador de párrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Usar separadores de línea y de párrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279496"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="f2738-105">Usar separadores de línea y de párrafo</span><span class="sxs-lookup"><span data-stu-id="f2738-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="f2738-106">Las aplicaciones deben usar el carácter separador de línea (0x2028) y el carácter separador de párrafo (0x2029) para dividir el texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="f2738-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="f2738-107">Se inicia una nueva línea después de cada separador de línea.</span><span class="sxs-lookup"><span data-stu-id="f2738-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="f2738-108">Se inicia un nuevo párrafo detrás de cada separador de párrafo.</span><span class="sxs-lookup"><span data-stu-id="f2738-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="f2738-109">No es necesario iniciar la primera línea o párrafo de un archivo con estos caracteres o finalizar la última línea o párrafo.</span><span class="sxs-lookup"><span data-stu-id="f2738-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="f2738-110">Si lo hace, indicará que hay una línea o un párrafo vacíos en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="f2738-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="f2738-111">La aplicación puede utilizar el separador de línea para indicar un final de línea incondicional.</span><span class="sxs-lookup"><span data-stu-id="f2738-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="f2738-112">Sin embargo, los separadores de línea no se corresponden con los caracteres de avance de línea y retorno de carro independientes o una combinación de estos caracteres.</span><span class="sxs-lookup"><span data-stu-id="f2738-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="f2738-113">Los separadores de línea se deben procesar por separado de los caracteres de avance de línea y retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="f2738-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="f2738-114">La aplicación puede insertar un separador de párrafo entre párrafos de texto.</span><span class="sxs-lookup"><span data-stu-id="f2738-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="f2738-115">El uso de este separador permite la creación de archivos de texto sin formato que se pueden formatear con anchos de línea diferentes en diferentes sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="f2738-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="f2738-116">El sistema de destino puede hacer caso omiso de los separadores de línea y realizar saltos entre párrafos solo en los separadores de párrafo.</span><span class="sxs-lookup"><span data-stu-id="f2738-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2738-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2738-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2738-118">Usar caracteres especiales en Unicode</span><span class="sxs-lookup"><span data-stu-id="f2738-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



