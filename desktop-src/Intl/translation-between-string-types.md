---
description: Las funciones enumeradas en la tabla siguiente traducen cadenas de caracteres de un tipo de cadena a otro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversión entre tipos de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687610"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="59e46-103">Conversión entre tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="59e46-103">Translation Between String Types</span></span>

<span data-ttu-id="59e46-104">Las funciones enumeradas en la tabla siguiente traducen cadenas de caracteres de un tipo de cadena a otro.</span><span class="sxs-lookup"><span data-stu-id="59e46-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="59e46-105">Función</span><span class="sxs-lookup"><span data-stu-id="59e46-105">Function</span></span>                                           | <span data-ttu-id="59e46-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="59e46-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="59e46-107">**FoldString**</span><span class="sxs-lookup"><span data-stu-id="59e46-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="59e46-108">Convierte una cadena de caracteres en otra.</span><span class="sxs-lookup"><span data-stu-id="59e46-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="59e46-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="59e46-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="59e46-110">Asigna una cadena de caracteres por configuración regional.</span><span class="sxs-lookup"><span data-stu-id="59e46-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="59e46-111">**ToUnicode**</span><span class="sxs-lookup"><span data-stu-id="59e46-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="59e46-112">Traduce un código de tecla virtual en un carácter Unicode.</span><span class="sxs-lookup"><span data-stu-id="59e46-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="59e46-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="59e46-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="59e46-114">Asigna una cadena multibyte a una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="59e46-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="59e46-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="59e46-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="59e46-116">Asigna una cadena Unicode a una cadena multibyte.</span><span class="sxs-lookup"><span data-stu-id="59e46-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="59e46-117">Las funciones [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) y [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) son especialmente útiles para las aplicaciones que admiten varios tipos de cadena.</span><span class="sxs-lookup"><span data-stu-id="59e46-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="59e46-118">ANSI C también define las funciones de conversión **wcstombs** y **mbstowcs**, pero solo se pueden convertir en y desde el juego de caracteres compatible con la biblioteca estándar de C.</span><span class="sxs-lookup"><span data-stu-id="59e46-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59e46-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59e46-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e46-120">Unicode en la API de Windows</span><span class="sxs-lookup"><span data-stu-id="59e46-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
