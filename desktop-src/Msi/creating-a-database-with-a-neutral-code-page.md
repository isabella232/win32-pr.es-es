---
description: El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Crear una base de datos con una página de códigos neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082794"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="2da1e-103">Crear una base de datos con una página de códigos neutra</span><span class="sxs-lookup"><span data-stu-id="2da1e-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="2da1e-104">El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos.</span><span class="sxs-lookup"><span data-stu-id="2da1e-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="2da1e-105">A continuación, la base de datos se puede establecer en la página de códigos de la localización y se puede Agregar la información de localización como se describe en [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="2da1e-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="2da1e-106">Para crear una base de datos neutra, evite los caracteres extendidos que no pertenecen al Juego de caracteres ASCII y, por tanto, requieren una página de códigos especial.</span><span class="sxs-lookup"><span data-stu-id="2da1e-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="2da1e-107">Por ejemplo, el signo de copyright, el © y el signo de marca registrada,, no son caracteres ASCII y requieren una página de códigos ANSI especial para la presentación adecuada.</span><span class="sxs-lookup"><span data-stu-id="2da1e-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="2da1e-108">En su lugar, use (c) y (r), ya que estos caracteres se pueden traducir o transformar en los símbolos para la versión en inglés.</span><span class="sxs-lookup"><span data-stu-id="2da1e-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="2da1e-109">Esta base de datos neutra puede localizarse después configurando su página de códigos y agregando información de localización por edición de tabla o importando archivos de archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="2da1e-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



