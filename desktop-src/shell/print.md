---
description: La API de Shell proporciona funciones que se pueden usar para administrar impresoras en red. Si un archivo tiene asociado el verbo imprimir, puede usar el comando ShellExecuteEx para imprimirlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Administrar impresoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985638"
---
# <a name="managing-printers"></a><span data-ttu-id="f75e9-104">Administrar impresoras</span><span class="sxs-lookup"><span data-stu-id="f75e9-104">Managing Printers</span></span>

<span data-ttu-id="f75e9-105">La API de Shell proporciona funciones que se pueden usar para administrar impresoras en red.</span><span class="sxs-lookup"><span data-stu-id="f75e9-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="f75e9-106">Si un archivo tiene asociado el verbo **Imprimir** , puede usar el comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="f75e9-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="f75e9-107">Administración de impresoras</span><span class="sxs-lookup"><span data-stu-id="f75e9-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="f75e9-108">Imprimir archivos con ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f75e9-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="f75e9-109">Administración de impresoras</span><span class="sxs-lookup"><span data-stu-id="f75e9-109">Printer Management</span></span>

<span data-ttu-id="f75e9-110">Puede administrar impresoras en un sistema con la función [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) .</span><span class="sxs-lookup"><span data-stu-id="f75e9-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="f75e9-111">Esta función le permite:</span><span class="sxs-lookup"><span data-stu-id="f75e9-111">This function allows you to:</span></span>

-   <span data-ttu-id="f75e9-112">Instalar impresoras.</span><span class="sxs-lookup"><span data-stu-id="f75e9-112">Install printers.</span></span>
-   <span data-ttu-id="f75e9-113">Abra impresoras.</span><span class="sxs-lookup"><span data-stu-id="f75e9-113">Open printers.</span></span>
-   <span data-ttu-id="f75e9-114">Obtiene las propiedades de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f75e9-114">Get printer properties.</span></span>
-   <span data-ttu-id="f75e9-115">Crear vínculos de impresora.</span><span class="sxs-lookup"><span data-stu-id="f75e9-115">Create printer links.</span></span>
-   <span data-ttu-id="f75e9-116">Imprima una página de prueba.</span><span class="sxs-lookup"><span data-stu-id="f75e9-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="f75e9-117">Imprimir archivos con ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="f75e9-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="f75e9-118">Si un tipo de archivo tiene un comando de impresión asociado, puede imprimir el archivo llamando a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con **Print** como el verbo.</span><span class="sxs-lookup"><span data-stu-id="f75e9-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="f75e9-119">Este comando suele ser el mismo que el utilizado para el verbo **abierto** , con la adición de una marca para indicar a la aplicación que imprima el archivo.</span><span class="sxs-lookup"><span data-stu-id="f75e9-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="f75e9-120">Por ejemplo, Microsoft WordPad puede imprimir archivos. txt.</span><span class="sxs-lookup"><span data-stu-id="f75e9-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="f75e9-121">El verbo **Open** de un archivo. txt se correspondería a algo como el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="f75e9-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="f75e9-122">Cuando se usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir un archivo. txt, WordPad abre el archivo, lo imprime y, a continuación, lo cierra, y devuelve el control a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f75e9-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="f75e9-123">La siguiente función de ejemplo toma una ruta de acceso completa y usa **ShellExecuteEx** para imprimirla, mediante el comando Print asociado a su extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f75e9-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



