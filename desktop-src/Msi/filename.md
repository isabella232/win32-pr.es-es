---
description: El tipo de datos FILENAME es una cadena de texto que contiene un nombre de archivo o una carpeta.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544278"
---
# <a name="filename"></a><span data-ttu-id="f7cf1-103">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="f7cf1-103">Filename</span></span>

<span data-ttu-id="f7cf1-104">El tipo de datos FILENAME es una cadena de texto que contiene un nombre de archivo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="f7cf1-105">De forma predeterminada, se supone que el nombre de archivo usa la sintaxis de nombre de archivo corto; es decir, el nombre de ocho caracteres, el punto (.) y la extensión de 3 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="f7cf1-106">Siempre se debe proporcionar un nombre corto de archivo porque se puede establecer la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen de destino de la instalación solo puede admitir nombres de archivo cortos.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="f7cf1-107">Para incluir un nombre de archivo largo con el nombre de archivo corto, sepárelo del nombre de archivo corto con una barra vertical ( \| ).</span><span class="sxs-lookup"><span data-stu-id="f7cf1-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="f7cf1-108">Por ejemplo, las dos cadenas siguientes son válidas:</span><span class="sxs-lookup"><span data-stu-id="f7cf1-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="f7cf1-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="f7cf1-109">status.txt</span></span>
-   <span data-ttu-id="f7cf1-110">Project ~1.txt\| Status.txt de proyecto</span><span class="sxs-lookup"><span data-stu-id="f7cf1-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="f7cf1-111">Los nombres de archivo cortos y largos no deben contener los caracteres siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7cf1-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="f7cf1-112">barra diagonal (/) o ( \\ )</span><span class="sxs-lookup"><span data-stu-id="f7cf1-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="f7cf1-113">signo de interrogación (?)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-113">question mark (?)</span></span>
-   <span data-ttu-id="f7cf1-114">barra vertical ( \| )</span><span class="sxs-lookup"><span data-stu-id="f7cf1-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="f7cf1-115">corchete angular de cierre (>)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="f7cf1-116">corchete angular de apertura (<)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="f7cf1-117">dos puntos (:)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-117">colon (:)</span></span>
-   <span data-ttu-id="f7cf1-118">asterisco ( \* )</span><span class="sxs-lookup"><span data-stu-id="f7cf1-118">asterisk (\*)</span></span>
-   <span data-ttu-id="f7cf1-119">comillas dobles (")</span><span class="sxs-lookup"><span data-stu-id="f7cf1-119">quotation mark (")</span></span>

<span data-ttu-id="f7cf1-120">Además, los nombres de archivo cortos no deben contener los caracteres siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7cf1-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="f7cf1-121">signo más (+)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-121">plus sign (+)</span></span>
-   <span data-ttu-id="f7cf1-122">coma (,)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-122">comma (,)</span></span>
-   <span data-ttu-id="f7cf1-123">punto y coma (;)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-123">semicolon (;)</span></span>
-   <span data-ttu-id="f7cf1-124">signo igual (=)</span><span class="sxs-lookup"><span data-stu-id="f7cf1-124">equals sign (=)</span></span>
-   <span data-ttu-id="f7cf1-125">corchete de apertura ( \[ )</span><span class="sxs-lookup"><span data-stu-id="f7cf1-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="f7cf1-126">corchete de cierre ( \] )</span><span class="sxs-lookup"><span data-stu-id="f7cf1-126">right square bracket (\])</span></span>

<span data-ttu-id="f7cf1-127">No se permite ningún espacio delante del \| separador de barra vertical () para la sintaxis de nombre de archivo corto/nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="f7cf1-128">Los nombres de archivo cortos no pueden incluir un espacio, aunque puede ser un nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="f7cf1-129">Solo puede existir un espacio después del separador si el nombre de archivo largo del nombre de archivo comienza con el espacio.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="f7cf1-130">No se permite la sintaxis de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="f7cf1-131">El formato de la columna FileName de la tabla [MsiEmbeddedUI](msiembeddedui-table.md) es similar al tipo de datos Format FILENAME, excepto \| en que no está disponible el separador de barra vertical () para la sintaxis de nombre de archivo corto/nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="f7cf1-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



