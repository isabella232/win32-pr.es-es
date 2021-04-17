---
title: Buscar archivos
description: De forma predeterminada, RC busca en primer lugar los archivos de encabezado y los archivos de recursos (como los archivos de icono y de cursor) en el directorio actual y, después, en los directorios especificados por la variable de entorno INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704737"
---
# <a name="searching-for-files"></a><span data-ttu-id="630ae-103">Buscar archivos</span><span class="sxs-lookup"><span data-stu-id="630ae-103">Searching for Files</span></span>

<span data-ttu-id="630ae-104">De forma predeterminada, RC busca en primer lugar los archivos de encabezado y los archivos de recursos (como los archivos de icono y de cursor) en el directorio actual y, después, en los directorios especificados por la variable de entorno INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="630ae-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="630ae-105">(La variable de entorno PATH no tiene ningún efecto en qué directorios busca en RC).</span><span class="sxs-lookup"><span data-stu-id="630ae-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="630ae-106">Agregar un directorio para buscar</span><span class="sxs-lookup"><span data-stu-id="630ae-106">Adding a Directory to Search</span></span>

<span data-ttu-id="630ae-107">Puede usar la opción **/i** para agregar un directorio a la lista de directorios de búsquedas RC.</span><span class="sxs-lookup"><span data-stu-id="630ae-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="630ae-108">Después, el compilador busca en los directorios en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="630ae-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="630ae-109">Directorio actual</span><span class="sxs-lookup"><span data-stu-id="630ae-109">The current directory</span></span>
2.  <span data-ttu-id="630ae-110">Directorio o directorios que se especifican mediante la opción **/i** , en el orden en que aparecen en la línea de comandos de RC</span><span class="sxs-lookup"><span data-stu-id="630ae-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="630ae-111">La lista de directorios especificados por la variable de entorno INCLUDE, en el orden en que la variable los muestra, a menos que especifique la opción **/x**</span><span class="sxs-lookup"><span data-stu-id="630ae-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="630ae-112">En el ejemplo siguiente se compila el archivo de definición de recursos MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="630ae-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="630ae-113">**rc/i c: \\ contenido de origen \\ /i d: \\ Resources MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="630ae-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="630ae-114">Al compilar el script MyApp. rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual, en C: \\ source \\ Materials and D: \\ Resources y, a continuación, en los directorios especificados por la variable de entorno include.</span><span class="sxs-lookup"><span data-stu-id="630ae-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="630ae-115">Omitir la variable de entorno INCLUDE</span><span class="sxs-lookup"><span data-stu-id="630ae-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="630ae-116">Puede evitar que RC use la variable de entorno INCLUDE al determinar los directorios en los que buscar.</span><span class="sxs-lookup"><span data-stu-id="630ae-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="630ae-117">Para ello, use la opción **/x** .</span><span class="sxs-lookup"><span data-stu-id="630ae-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="630ae-118">A continuación, el compilador busca los archivos solo en el directorio actual y en los directorios especificados mediante la opción **/i** .</span><span class="sxs-lookup"><span data-stu-id="630ae-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="630ae-119">El siguiente comando compila el archivo de script MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="630ae-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="630ae-120">**RC/x/i c: \\ código fuente \\ MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="630ae-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="630ae-121">Al compilar el script MyApp. rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual y, después, en C: \\ source \\ materials.</span><span class="sxs-lookup"><span data-stu-id="630ae-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="630ae-122">No busca en los directorios especificados por la variable de entorno INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="630ae-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




