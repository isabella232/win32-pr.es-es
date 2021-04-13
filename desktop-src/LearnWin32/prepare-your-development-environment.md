---
title: Preparación del entorno de desarrollo
description: Preparación del entorno de desarrollo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358906"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="19a42-103">Preparación del entorno de desarrollo</span><span class="sxs-lookup"><span data-stu-id="19a42-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="19a42-104">Para escribir un programa de Windows en C o C++, debe instalar el kit de desarrollo de software (SDK) de Microsoft Windows o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="19a42-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="19a42-105">El Windows SDK contiene los encabezados y las bibliotecas necesarios para compilar y vincular la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19a42-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="19a42-106">El Windows SDK también contiene herramientas de línea de comandos para compilar aplicaciones de Windows, incluidas la Visual C++ compilador y el vinculador.</span><span class="sxs-lookup"><span data-stu-id="19a42-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="19a42-107">Aunque puede compilar y compilar programas de Windows con las herramientas de línea de comandos, se recomienda usar Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="19a42-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="19a42-108">Puede descargar una descarga gratuita de Visual Studio Community o pruebas gratuitas de otras versiones de Visual Studio [aquí](https://visualstudio.microsoft.com/downloads/).</span><span class="sxs-lookup"><span data-stu-id="19a42-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="19a42-109">Cada versión de la Windows SDK tiene como destino la versión más reciente de Windows, así como varias versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="19a42-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="19a42-110">En las notas de la versión se enumeran las plataformas específicas que se admiten, pero a menos que esté manteniendo una aplicación para una versión anterior de Windows, debe instalar la versión más reciente de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="19a42-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="19a42-111">Puede descargar la Windows SDK más reciente [aquí](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="19a42-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="19a42-112">El Windows SDK admite el desarrollo de aplicaciones de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="19a42-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="19a42-113">Las API de Windows están diseñadas para que el mismo código se pueda compilar para 32 bits o 64 bits sin cambios.</span><span class="sxs-lookup"><span data-stu-id="19a42-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="19a42-114">El Windows SDK no admite el desarrollo de controladores de hardware, y esta serie no tratará el desarrollo de controladores.</span><span class="sxs-lookup"><span data-stu-id="19a42-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="19a42-115">Para obtener información acerca de cómo escribir un controlador de hardware, consulte [Introducción con controladores de Windows](/windows-hardware/drivers/gettingstarted/).</span><span class="sxs-lookup"><span data-stu-id="19a42-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="19a42-116">Siguientes</span><span class="sxs-lookup"><span data-stu-id="19a42-116">Next</span></span>

[<span data-ttu-id="19a42-117">Convenciones de codificación de Windows</span><span class="sxs-lookup"><span data-stu-id="19a42-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="19a42-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19a42-118">Related topics</span></span>

* [<span data-ttu-id="19a42-119">Descarga de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19a42-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="19a42-120">Descargar Windows SDK</span><span class="sxs-lookup"><span data-stu-id="19a42-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)