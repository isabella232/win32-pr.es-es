---
description: Las siguientes funciones se usan con juegos de caracteres.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funciones de juego de caracteres y Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083193"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="e0886-103">Funciones de juego de caracteres y Unicode</span><span class="sxs-lookup"><span data-stu-id="e0886-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="e0886-104">Las siguientes funciones se usan con juegos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e0886-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="e0886-105">Función</span><span class="sxs-lookup"><span data-stu-id="e0886-105">Function</span></span>                                                       | <span data-ttu-id="e0886-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0886-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0886-107">**GetTextCharset**</span><span class="sxs-lookup"><span data-stu-id="e0886-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="e0886-108">Recupera un identificador de juego de caracteres para la fuente seleccionada actualmente en un contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e0886-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="e0886-109">**GetTextCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0886-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="e0886-110">Recupera información sobre el juego de caracteres de la fuente seleccionada actualmente en un contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e0886-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="e0886-111">**IsDBCSLeadByte**</span><span class="sxs-lookup"><span data-stu-id="e0886-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="e0886-112">Determina si un carácter especificado es un byte inicial de la página de códigos ANSI de Windows predeterminada del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="e0886-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="e0886-113">**IsDBCSLeadByteEx**</span><span class="sxs-lookup"><span data-stu-id="e0886-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="e0886-114">Determina si un carácter especificado es potencialmente un byte inicial.</span><span class="sxs-lookup"><span data-stu-id="e0886-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="e0886-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="e0886-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="e0886-116">Determina si es probable que un búfer contenga una forma de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0886-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="e0886-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="e0886-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="e0886-118">Asigna una cadena de caracteres a una cadena UTF-16 (carácter ancho).</span><span class="sxs-lookup"><span data-stu-id="e0886-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="e0886-119">**TranslateCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="e0886-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="e0886-120">Traduce la información del juego de caracteres y establece todos los miembros de una estructura de destino en los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="e0886-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="e0886-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="e0886-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="e0886-122">Asigna una cadena UTF-16 (carácter ancho) a una nueva cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e0886-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="e0886-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0886-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="e0886-124">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="e0886-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="e0886-125">**NlsDllCodePageTranslation**</span><span class="sxs-lookup"><span data-stu-id="e0886-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="e0886-126">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="e0886-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="e0886-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0886-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="e0886-128">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="e0886-128">Do not use.</span></span>                                                                                                           |



 

 

 
