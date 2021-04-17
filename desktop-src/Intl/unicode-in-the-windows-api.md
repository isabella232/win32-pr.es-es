---
description: 'Las funciones de la API de Windows que manipulan caracteres suelen implementarse en uno de los tres formatos siguientes:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode en la API de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687933"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="16091-103">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="16091-103">Unicode in the Windows API</span></span>

<span data-ttu-id="16091-104">Las funciones de la API de Windows que manipulan caracteres suelen implementarse en uno de los tres formatos siguientes:</span><span class="sxs-lookup"><span data-stu-id="16091-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="16091-105">Una versión genérica que se puede compilar para páginas de códigos de Windows o Unicode</span><span class="sxs-lookup"><span data-stu-id="16091-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="16091-106">Una versión de [Página de códigos de Windows](code-pages.md) con la letra "a" que se usa para indicar "ANSI"</span><span class="sxs-lookup"><span data-stu-id="16091-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="16091-107">Una versión [Unicode](unicode.md) con la letra "W" utilizada para indicar "Wide"</span><span class="sxs-lookup"><span data-stu-id="16091-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="16091-108">Algunas funciones más recientes solo admiten versiones Unicode.</span><span class="sxs-lookup"><span data-stu-id="16091-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="16091-109">Para obtener más información, vea [convenciones de los prototipos de función](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="16091-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="16091-110">En los temas siguientes se describen los tipos de datos Unicode y cómo se usan en funciones y mensajes; el uso de recursos, nombres de archivo y argumentos de la línea de comandos; y métodos de traducción entre distintos tipos de cadenas.</span><span class="sxs-lookup"><span data-stu-id="16091-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="16091-111">Traducción automática de mensajes</span><span class="sxs-lookup"><span data-stu-id="16091-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="16091-112">Juegos de caracteres usados en nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="16091-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="16091-113">Argumentos de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="16091-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="16091-114">Convenciones para Prototipos de función</span><span class="sxs-lookup"><span data-stu-id="16091-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="16091-115">Funciones estándar de C</span><span class="sxs-lookup"><span data-stu-id="16091-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="16091-116">Diferencias de las funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="16091-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="16091-117">Conversión entre tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="16091-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="16091-118">Tipos de datos de Windows para cadenas</span><span class="sxs-lookup"><span data-stu-id="16091-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="16091-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16091-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16091-120">Acerca de los juegos de caracteres y Unicode</span><span class="sxs-lookup"><span data-stu-id="16091-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



