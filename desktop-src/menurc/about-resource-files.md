---
title: Acerca de los archivos de recursos
description: Describe cómo incluir recursos en una aplicación basada en Windows con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075727"
---
# <a name="about-resource-files"></a><span data-ttu-id="a02fb-103">Acerca de los archivos de recursos</span><span class="sxs-lookup"><span data-stu-id="a02fb-103">About Resource Files</span></span>

<span data-ttu-id="a02fb-104">Para incluir recursos en la aplicación basada en Windows con RC, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a02fb-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="a02fb-105">Cree archivos individuales para los cursores, iconos, mapas de bits, cuadros de diálogo y fuentes.</span><span class="sxs-lookup"><span data-stu-id="a02fb-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="a02fb-106">Cree un script de definición de recursos (archivo. RC) que describa los recursos utilizados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a02fb-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="a02fb-107">Compile el script con RC.</span><span class="sxs-lookup"><span data-stu-id="a02fb-107">Compile the script with RC.</span></span> <span data-ttu-id="a02fb-108">Para obtener más información, consulte [uso de RC (la línea de comandos de RC)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="a02fb-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="a02fb-109">Vincule el archivo de recursos compilado (. res) al archivo ejecutable de la aplicación con el enlazador.</span><span class="sxs-lookup"><span data-stu-id="a02fb-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="a02fb-110">Un archivo de recursos es un archivo de texto con la extensión. rc.</span><span class="sxs-lookup"><span data-stu-id="a02fb-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="a02fb-111">El archivo puede utilizar caracteres de un solo byte, de doble byte o Unicode.</span><span class="sxs-lookup"><span data-stu-id="a02fb-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="a02fb-112">La sintaxis y la semántica del preprocesador RC son similares a las del compilador de C/C++ de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a02fb-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="a02fb-113">Sin embargo, RC admite un subconjunto de las directivas de preprocesador, define y pragma en un script.</span><span class="sxs-lookup"><span data-stu-id="a02fb-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="a02fb-114">El archivo de script define los recursos.</span><span class="sxs-lookup"><span data-stu-id="a02fb-114">The script file defines resources.</span></span> <span data-ttu-id="a02fb-115">En el caso de un recurso que se encuentre en un archivo independiente, como un icono o un cursor, el script especifica el recurso y el archivo que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="a02fb-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="a02fb-116">En algunos recursos, como un menú, la definición completa del recurso existe en el script.</span><span class="sxs-lookup"><span data-stu-id="a02fb-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="a02fb-117">En los temas siguientes se describe la información que puede contener un archivo de script:</span><span class="sxs-lookup"><span data-stu-id="a02fb-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="a02fb-118">[Comentarios](comments.md), que son notas que RC omitirá.</span><span class="sxs-lookup"><span data-stu-id="a02fb-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="a02fb-119">[Macros predefinidas](predefined-macros.md), que no toman ningún argumento y no se pueden redefinir.</span><span class="sxs-lookup"><span data-stu-id="a02fb-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="a02fb-120">[Directivas de preprocesador](preprocessor-directives.md), que indican a RC que realice acciones en el script antes de compilarlo.</span><span class="sxs-lookup"><span data-stu-id="a02fb-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="a02fb-121">[Operadores de preprocesador](preprocessor-operators.md), que se usan con la Directiva de **\# definición** .</span><span class="sxs-lookup"><span data-stu-id="a02fb-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="a02fb-122">Directivas pragma</span><span class="sxs-lookup"><span data-stu-id="a02fb-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="a02fb-123">[Instrucciones de definición de recursos](resource-definition-statements.md), que denominan y describen los recursos.</span><span class="sxs-lookup"><span data-stu-id="a02fb-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




