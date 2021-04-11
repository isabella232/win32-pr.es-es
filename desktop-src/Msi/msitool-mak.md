---
description: MSITool. Mak es un archivo make que se puede usar para compilar herramientas y acciones personalizadas.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: MSITool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156153"
---
# <a name="msitoolmak"></a><span data-ttu-id="acba3-103">MSITool. Mak</span><span class="sxs-lookup"><span data-stu-id="acba3-103">Msitool.mak</span></span>

<span data-ttu-id="acba3-104">MSITool. Mak es un archivo make que se puede usar para compilar herramientas y acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="acba3-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="acba3-105">Se puede usar con Visual C++ versión 4,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="acba3-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="acba3-106">Para obtener más información, vea el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="acba3-106">For more information, see the header file.</span></span> <span data-ttu-id="acba3-107">Requiere que se defina un conjunto de valores antes de incluir este archivo.</span><span class="sxs-lookup"><span data-stu-id="acba3-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="acba3-108">Normalmente, los desarrolladores colocan al principio de. cpp, ifdef que se omitirá en el compilador de C.</span><span class="sxs-lookup"><span data-stu-id="acba3-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="acba3-109">Del mismo modo, los recursos se agregan al final del archivo. cpp.</span><span class="sxs-lookup"><span data-stu-id="acba3-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="acba3-110">Vea los ejemplos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="acba3-110">See samples for details.</span></span>

<span data-ttu-id="acba3-111">VCBIN se puede definir en el directorio donde se encuentran las herramientas de Visual C++ o el archivo make usa MSVCDIR y MSDEVDIR.</span><span class="sxs-lookup"><span data-stu-id="acba3-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="acba3-112">Si no están definidas, no especifica ninguna ubicación, suponiendo que las herramientas estén en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="acba3-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="acba3-113">Un problema con las variables de entorno en Visual C++ versión 5,0 es que si ambos no están en su ruta de acceso, el enlazador no puede encontrar Msdis100.dll.</span><span class="sxs-lookup"><span data-stu-id="acba3-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="acba3-114">Si lo copia de MSDEVDIR a MSVCDIR, funcionará.</span><span class="sxs-lookup"><span data-stu-id="acba3-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="acba3-115">La otra opción es copiar Msdis100.dll y Rc.exe y Rcdll.dll en MSVCDIR, y establecer VCBIN en ese.</span><span class="sxs-lookup"><span data-stu-id="acba3-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="acba3-116">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="acba3-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acba3-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acba3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acba3-118">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="acba3-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="acba3-119">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="acba3-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



