---
description: Una página de códigos es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de carácter.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Comprobar la página de códigos de la base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666997"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="c35aa-103">Comprobar la página de códigos de la base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="c35aa-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="c35aa-104">Una *Página de códigos* es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de carácter.</span><span class="sxs-lookup"><span data-stu-id="c35aa-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="c35aa-105">Diferentes páginas de códigos proporcionan compatibilidad con los juegos de caracteres que se usan en diferentes países o regiones.</span><span class="sxs-lookup"><span data-stu-id="c35aa-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="c35aa-106">Se hace referencia a las páginas de códigos por número; por ejemplo, la página de códigos 932 representa el juego de caracteres japoneses y la página de códigos 950 representa uno de los juegos de caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="c35aa-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="c35aa-107">Consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos ASCII.</span><span class="sxs-lookup"><span data-stu-id="c35aa-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="c35aa-108">Se puede usar la misma página de códigos ASCII, 1252 para inglés y francés.</span><span class="sxs-lookup"><span data-stu-id="c35aa-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="c35aa-109">Por lo tanto, no es necesario restablecer la página de códigos del MNP2000.msi de base de datos (Inglés) para cambiar la instalación a francés.</span><span class="sxs-lookup"><span data-stu-id="c35aa-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="c35aa-110">Para obtener más información sobre cómo establecer la página de códigos [, vea control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="c35aa-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="c35aa-111">Continuar</span><span class="sxs-lookup"><span data-stu-id="c35aa-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



