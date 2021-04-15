---
description: Antes de que las funciones de configuración puedan tener acceso a la información del archivo INF, debe abrirlo con una llamada a la función SetupOpenInfFile. Esta función devuelve un identificador al archivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Abrir y cerrar un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545790"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="44815-104">Abrir y cerrar un archivo INF</span><span class="sxs-lookup"><span data-stu-id="44815-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="44815-105">Antes de que las funciones de configuración puedan tener acceso a la información del archivo INF, debe abrirlo con una llamada a la función [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) .</span><span class="sxs-lookup"><span data-stu-id="44815-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="44815-106">Esta función devuelve un identificador al archivo INF.</span><span class="sxs-lookup"><span data-stu-id="44815-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="44815-107">Si no conoce el nombre del archivo INF que necesita abrir, puede usar la función [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obtener una lista de archivos INF en un directorio.</span><span class="sxs-lookup"><span data-stu-id="44815-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="44815-108">Después de abrir un archivo INF, puede anexar más archivos INF al archivo INF abierto mediante la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) .</span><span class="sxs-lookup"><span data-stu-id="44815-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="44815-109">Es funcionalmente similar a una instrucción include.</span><span class="sxs-lookup"><span data-stu-id="44815-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="44815-110">Cuando las siguientes funciones de instalación hagan referencia a un archivo INF abierto, también podrán tener acceso a cualquier información almacenada en los archivos anexados.</span><span class="sxs-lookup"><span data-stu-id="44815-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="44815-111">Si no especifica un archivo INF durante la llamada a la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** anexa los archivos especificados por la clave **LayoutFile** en la sección **versión** del archivo INF abierto.</span><span class="sxs-lookup"><span data-stu-id="44815-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="44815-112">Cuando ya no necesite la información del archivo INF, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar los recursos asignados durante la llamada a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span><span class="sxs-lookup"><span data-stu-id="44815-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



