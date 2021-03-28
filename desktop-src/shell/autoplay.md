---
description: La ejecución automática es una característica del sistema operativo Windows.
title: Creación de una aplicación de CD-ROM habilitada para AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275250"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="4b858-103">Creación de una aplicación de CD-ROM habilitada para AutoRun</span><span class="sxs-lookup"><span data-stu-id="4b858-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="4b858-104">La ejecución automática es una característica del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="4b858-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="4b858-105">Automatiza los procedimientos para instalar y configurar productos diseñados para plataformas basadas en Windows que se distribuyen en CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="4b858-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="4b858-106">Cuando los usuarios insertan un disco compacto habilitado para la ejecución automática en la unidad de CD-ROM, el programa de ejecución automática ejecuta automáticamente una aplicación en el CD-ROM que instala, configura o ejecuta el producto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4b858-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="4b858-107">La ejecución automática se puede usar para instalar y ejecutar aplicaciones de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="4b858-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="4b858-108">Aunque la ejecución automática se usa normalmente para las aplicaciones Windows, también se puede usar para instalar, configurar o ejecutar aplicaciones basadas en MS-DOS en una sesión de Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="4b858-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="4b858-109">Puede configurar cada aplicación basada en MS-DOS con su propio icono único, Config.sys archivo y Autoexec.bat archivo.</span><span class="sxs-lookup"><span data-stu-id="4b858-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="4b858-110">Windows crea los archivos de configuración correctos para la aplicación basada en MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="4b858-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="4b858-111">A continuación, la aplicación de inicio inicia la aplicación basada en MS-dos en una ventana de.</span><span class="sxs-lookup"><span data-stu-id="4b858-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="4b858-112">Para que la ejecución automática funcione, la unidad de CD-ROM debe tener controladores de dispositivos de 32 o 64 bits que detecten Cuándo un usuario inserta un disco compacto y notifica al sistema.</span><span class="sxs-lookup"><span data-stu-id="4b858-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="4b858-113">En las secciones siguientes se describe cómo implementar una aplicación de CD-ROM habilitada para AutoRun.</span><span class="sxs-lookup"><span data-stu-id="4b858-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="4b858-114">Creación de una aplicación AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="4b858-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="4b858-115">Entradas Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="4b858-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="4b858-116">Habilitar y deshabilitar la ejecución automática</span><span class="sxs-lookup"><span data-stu-id="4b858-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



