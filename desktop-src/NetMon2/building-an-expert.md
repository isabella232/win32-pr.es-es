---
description: En este tema se describe cómo crear un experto genérico que se incluye con el SDK de Monitor de red.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creación de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276698"
---
# <a name="building-an-expert"></a><span data-ttu-id="42f0a-103">Creación de un experto</span><span class="sxs-lookup"><span data-stu-id="42f0a-103">Building an Expert</span></span>

<span data-ttu-id="42f0a-104">En este tema se describe cómo crear un experto genérico que se incluye con el SDK de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="42f0a-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="42f0a-105">Antes de crear los siguientes ejemplos de código, instale el SDK de Monitor de red e inicialice el archivo de MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="42f0a-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="42f0a-106">**Para compilar un experto genérico**</span><span class="sxs-lookup"><span data-stu-id="42f0a-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="42f0a-107">Abra un símbolo del sistema de Monitor de red y navegue hasta el \\ subdirectorio Experts; por ejemplo, C: \\ archivos de programa \\ NetMonSDK2 \\ Experts.</span><span class="sxs-lookup"><span data-stu-id="42f0a-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="42f0a-108">Escriba **xcopy/e/s/V Blrplate**, a continuación, cuando se le solicite, escriba **D**.</span><span class="sxs-lookup"><span data-stu-id="42f0a-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="42f0a-109">Desplácese al \\ subdirectorio de mi experto.</span><span class="sxs-lookup"><span data-stu-id="42f0a-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="42f0a-110">Escriba **ren Blrplate \* . \* Mi experto \* . \***</span><span class="sxs-lookup"><span data-stu-id="42f0a-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="42f0a-111">Asegúrese de que se ha cambiado el nombre de todos los archivos correctamente.</span><span class="sxs-lookup"><span data-stu-id="42f0a-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="42f0a-112">Compruebe los nombres de archivo comparando los archivos del \\ \\ subdirectorio Experts Blrplate.</span><span class="sxs-lookup"><span data-stu-id="42f0a-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="42f0a-113">Modifique el archivo make reemplazando todas las apariciones de **Blrplate** por mi **experto**.</span><span class="sxs-lookup"><span data-stu-id="42f0a-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="42f0a-114">Edite ambos archivos. cpp reemplazando todas las apariciones de **Blrplate** por mi **experto**.</span><span class="sxs-lookup"><span data-stu-id="42f0a-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="42f0a-115">Tenga en cuenta que el identificador del cuadro de diálogo en config. cpp debe escribirse en mayúsculas (por ejemplo, mi **experto**).</span><span class="sxs-lookup"><span data-stu-id="42f0a-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="42f0a-116">Edite el. h reemplazando todas las apariciones de **Blrplate** por mi **experto**.</span><span class="sxs-lookup"><span data-stu-id="42f0a-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="42f0a-117">Edite Resrc1. h cambiando el nombre de **BLRPLATE** a mi **experto**.</span><span class="sxs-lookup"><span data-stu-id="42f0a-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="42f0a-118">(Recuerde que **debe** escribirse en mayúsculas).</span><span class="sxs-lookup"><span data-stu-id="42f0a-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="42f0a-119">Edite el archivo de mi experto. RC cambiando el nombre del cuadro de diálogo de configuración de BLRPLATE de IDD al cuadro de **\_ \_ \_ diálogo de configuración de IDD**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42f0a-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="42f0a-120">Escriba **NMake** para compilar el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="42f0a-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="42f0a-121">Para comprobar la compilación, cambie el directorio al \\ subdirectorio obj y compruebe que el archivo existe.</span><span class="sxs-lookup"><span data-stu-id="42f0a-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="42f0a-122">Para obtener más información, vea [Ver propiedades de archivos dll de expertos](viewing-expert-dll-properties.md).</span><span class="sxs-lookup"><span data-stu-id="42f0a-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="42f0a-123">Una vez completada la compilación, tendrá un archivo DLL experto que podrá probar e implementar con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="42f0a-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="42f0a-124">Para obtener más información acerca de cómo instalar un experto, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="42f0a-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="42f0a-125">Para obtener más información sobre cómo depurar un experto, consulte [depuración de un experto](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="42f0a-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



