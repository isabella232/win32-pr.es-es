---
title: Archivos de respuesta
description: Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL del compilador MIDL, archivos de respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387083"
---
# <a name="response-files"></a><span data-ttu-id="8c600-104">Archivos de respuesta</span><span class="sxs-lookup"><span data-stu-id="8c600-104">Response Files</span></span>

<span data-ttu-id="8c600-105">Como alternativa a colocar todas las opciones en la línea de comandos, el compilador MIDL acepta archivos de respuesta que contienen modificadores y argumentos.</span><span class="sxs-lookup"><span data-stu-id="8c600-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="8c600-106">Un archivo de respuesta es un archivo de texto que contiene una o varias opciones de línea de comandos del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="8c600-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="8c600-107">A diferencia de una línea de comandos, un archivo de respuesta permite varias líneas de opciones y nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="8c600-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="8c600-108">Esto puede ser útil debido a las limitaciones del entorno de compilación o por comodidad para el proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="8c600-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="8c600-109">Puede especificar un archivo de respuesta MIDL como:</span><span class="sxs-lookup"><span data-stu-id="8c600-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="8c600-110">**midl** **\@ filename**</span><span class="sxs-lookup"><span data-stu-id="8c600-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="8c600-111"><span id="filename"></span><span id="FILENAME"></span>*Nombre*</span><span class="sxs-lookup"><span data-stu-id="8c600-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="8c600-112">Especifica el nombre del archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c600-112">Specifies the name of the response file.</span></span> <span data-ttu-id="8c600-113">El nombre del archivo de respuesta debe seguir inmediatamente el carácter @ sin espacio en blanco entre el carácter @ y el nombre del archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c600-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="8c600-114">Las opciones de un archivo de respuesta se interpretan como si estuvieran presentes en ese lugar en la línea de comandos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="8c600-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="8c600-115">Cada argumento de un archivo de respuesta debe comenzar y terminar en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="8c600-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="8c600-116">No se puede usar el carácter de barra diagonal inversa ( \\ ) para concatenar líneas.</span><span class="sxs-lookup"><span data-stu-id="8c600-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="8c600-117">MIDL admite argumentos de línea de comandos que incluyen uno o varios archivos de respuesta, combinados con otros modificadores de línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="8c600-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="8c600-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="8c600-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="8c600-119">El compilador MIDL no admite archivos de respuesta anidados.</span><span class="sxs-lookup"><span data-stu-id="8c600-119">The MIDL compiler does not support nested response files.</span></span>

 

 




