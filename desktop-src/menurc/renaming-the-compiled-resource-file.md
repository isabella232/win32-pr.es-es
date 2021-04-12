---
title: Cambiar el nombre del archivo de recursos compilados
description: De forma predeterminada, al compilar recursos, RC nombra el archivo de recursos compilado (. res) con el nombre base del archivo. RC y lo coloca en el mismo directorio que el archivo. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268330"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="a6d59-103">Cambiar el nombre del archivo de recursos compilados</span><span class="sxs-lookup"><span data-stu-id="a6d59-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="a6d59-104">De forma predeterminada, al compilar recursos, RC nombra el archivo de recursos compilado (. res) con el nombre base del archivo. RC y lo coloca en el mismo directorio que el archivo. rc.</span><span class="sxs-lookup"><span data-stu-id="a6d59-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="a6d59-105">A continuación, se debe invocar CVTRES para convertir el archivo. res a un formato de recursos binario (. RBJ) que el enlazador puede entender.</span><span class="sxs-lookup"><span data-stu-id="a6d59-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="a6d59-106">En el ejemplo siguiente se compila MyApp. RC y se crea un archivo de recursos compilado denominado MyApp. res en el mismo directorio que MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="a6d59-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="a6d59-107">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="a6d59-107">**rc myapp.rc**</span></span>

<span data-ttu-id="a6d59-108">La opción **/FO** proporciona a el archivo. res resultante un nombre que difiere del nombre del archivo. RC correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a6d59-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="a6d59-109">Por ejemplo, para asignar un nombre al archivo. res resultante NewFile. res, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a6d59-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="a6d59-110">**RC-FO NewFile. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="a6d59-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="a6d59-111">La opción **/FO** también puede colocar el archivo. res en un directorio diferente.</span><span class="sxs-lookup"><span data-stu-id="a6d59-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="a6d59-112">Por ejemplo, el comando siguiente coloca el archivo de recursos compilado MyApp. res en el directorio C: \\ source \\ Resource:</span><span class="sxs-lookup"><span data-stu-id="a6d59-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="a6d59-113">**RC-FO c: \\ recurso de origen \\ \\ MyApp. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="a6d59-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




