---
description: Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Archivos de minivolcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152849"
---
# <a name="minidump-files"></a><span data-ttu-id="2d253-103">Archivos de minivolcado</span><span class="sxs-lookup"><span data-stu-id="2d253-103">Minidump Files</span></span>

<span data-ttu-id="2d253-104">Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado.</span><span class="sxs-lookup"><span data-stu-id="2d253-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="2d253-105">Las aplicaciones pueden crear archivos de minivolcado de manera muy rápida y eficaz.</span><span class="sxs-lookup"><span data-stu-id="2d253-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="2d253-106">Dado que los archivos de minivolcado son pequeños, se pueden enviar fácilmente a través de Internet a soporte técnico para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2d253-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="2d253-107">Un archivo de minivolcado no contiene tanta información como un archivo de volcado de memoria completo, pero contiene suficiente información para realizar operaciones de depuración básicas.</span><span class="sxs-lookup"><span data-stu-id="2d253-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="2d253-108">Para leer un archivo de minivolcado, debe tener los archivos binarios y de símbolos disponibles para el depurador.</span><span class="sxs-lookup"><span data-stu-id="2d253-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="2d253-109">Las versiones actuales de Microsoft Office y Microsoft Windows crean archivos de minivolcado con el fin de analizar los errores en los equipos de los clientes.</span><span class="sxs-lookup"><span data-stu-id="2d253-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="2d253-110">Las siguientes funciones DbgHelp se utilizan con archivos de minivolcado.</span><span class="sxs-lookup"><span data-stu-id="2d253-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="2d253-111">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="2d253-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="2d253-112">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="2d253-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="2d253-113">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="2d253-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



