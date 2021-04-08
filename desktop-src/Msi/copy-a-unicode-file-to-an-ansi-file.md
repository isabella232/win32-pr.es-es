---
description: El WiToAnsi.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. Este ejemplo muestra cómo se utiliza el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar un archivo Unicode en un archivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910710"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="6a093-104">Copiar un archivo Unicode en un archivo ANSI</span><span class="sxs-lookup"><span data-stu-id="6a093-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="6a093-105">El WiToAnsi.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6a093-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="6a093-106">Este ejemplo muestra cómo se utiliza el script para reescribir un archivo de texto Unicode como un archivo de texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="6a093-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="6a093-107">El uso de este ejemplo requiere la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="6a093-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="6a093-108">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="6a093-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="6a093-109">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="6a093-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="6a093-110">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="6a093-110">or if too few arguments are specified.</span></span> <span data-ttu-id="6a093-111">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ *ruta de acceso al archivo* \] .</span><span class="sxs-lookup"><span data-stu-id="6a093-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="6a093-112">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="6a093-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="6a093-113">**cscript WiToAnsi.vbs \[ ruta de acceso a la ruta de acceso del archivo Unicode \] \[ al archivo ANSI\]**</span><span class="sxs-lookup"><span data-stu-id="6a093-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="6a093-114">Especifique el archivo de texto Unicode que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="6a093-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="6a093-115">Especifique el archivo de texto ANSI que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6a093-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="6a093-116">Si no se especifica ningún archivo ANSI, se reemplaza el archivo Unicode.</span><span class="sxs-lookup"><span data-stu-id="6a093-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="6a093-117">Para obtener ejemplos de scripting adicionales, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6a093-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="6a093-118">En el caso de utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6a093-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



