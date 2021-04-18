---
title: Configuración del entorno
description: El kit de desarrollo de software (SDK) de la plataforma instalada proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de la plataforma que se puede ejecutar para configurar el entorno para la creación de aplicaciones que usan el SDK de la plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665631"
---
# <a name="environment-setup"></a><span data-ttu-id="c49f3-103">Configuración del entorno</span><span class="sxs-lookup"><span data-stu-id="c49f3-103">Environment Setup</span></span>

<span data-ttu-id="c49f3-104">El kit de desarrollo de software (SDK) de la plataforma instalada proporciona un archivo Setenv.bat ubicado en el directorio raíz del SDK de la plataforma que se puede ejecutar para configurar el entorno para la creación de aplicaciones que usan el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c49f3-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="c49f3-105">Configuración y variables</span><span class="sxs-lookup"><span data-stu-id="c49f3-105">Settings and Variables</span></span>

<span data-ttu-id="c49f3-106">También puede configurar manualmente el entorno agregando algo parecido a lo siguiente en el archivo de Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="c49f3-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="c49f3-107">Con Windows, puede editar el archivo de Autoexec.bat para incluir estos comandos.</span><span class="sxs-lookup"><span data-stu-id="c49f3-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="c49f3-108">Con Windows Server 2003, Windows XP, Windows 2000 o Windows NT, puede editar o agregar estos valores a las variables de entorno mediante el cuadro de diálogo del sistema que puede ejecutar desde el panel de control.</span><span class="sxs-lookup"><span data-stu-id="c49f3-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="c49f3-109">Esta configuración es adecuada para una plataforma Intel 80386 o posterior que ejecute Windows me, Windows 98 o Windows 95 con Microsoft Visual C++ y el SDK de la plataforma instalado.</span><span class="sxs-lookup"><span data-stu-id="c49f3-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="c49f3-110">Por ejemplo, en este sistema, Visual C++ versión 5,0 se instala en el directorio C: \\ MSDEV</span><span class="sxs-lookup"><span data-stu-id="c49f3-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="c49f3-111">El SDK de la plataforma se instala en el \\ directorio D: MSSDK.</span><span class="sxs-lookup"><span data-stu-id="c49f3-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="c49f3-112">La configuración del disco puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="c49f3-112">Your disk configuration may be different.</span></span> <span data-ttu-id="c49f3-113">Los directorios del SDK de la plataforma (para este ejemplo, los que tienen D: \\ MSSDK en ellos) se encuentran anteriormente en cada secuencia de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c49f3-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="c49f3-114">Esta secuencia presupone que las compilaciones de la línea de comandos están pensadas para ejecutarse en la ventana del símbolo del sistema y que los archivos de la biblioteca. h include y. lib del SDK de la plataforma son preferibles para esas compilaciones.</span><span class="sxs-lookup"><span data-stu-id="c49f3-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="c49f3-115">La variable de entorno CPU se define para controlar las compilaciones de Win32, dependiendo de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c49f3-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="c49f3-116">Los valores posibles actuales incluyen i386, MIPS, ALPHA y PPC.</span><span class="sxs-lookup"><span data-stu-id="c49f3-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="c49f3-117">Para obtener más información, vea el archivo Win32. Mak proporcionado en el SDK de la plataforma en el \\ Directorio de inclusión de MSSDK \\ .</span><span class="sxs-lookup"><span data-stu-id="c49f3-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="c49f3-118">Todos los archivos make de ejemplo de código del tutorial de COM incluyen Win32. Mak.</span><span class="sxs-lookup"><span data-stu-id="c49f3-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




