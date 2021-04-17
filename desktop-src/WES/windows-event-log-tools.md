---
title: Herramientas del registro de eventos de Windows
description: El registro de eventos de Windows proporciona las siguientes herramientas que se usan para compilar el proveedor.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104420492"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="8d790-103">Herramientas del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="8d790-103">Windows Event Log Tools</span></span>

<span data-ttu-id="8d790-104">El registro de eventos de Windows proporciona las siguientes herramientas que se usan para compilar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d790-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="8d790-105">Herramienta</span><span class="sxs-lookup"><span data-stu-id="8d790-105">Tool</span></span>                                                           | <span data-ttu-id="8d790-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d790-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d790-107">**Compilador de mensajes (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="8d790-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="8d790-108">Utilidad de línea de comandos que se usa para compilar manifiestos de instrumentación y archivos de texto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8d790-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="8d790-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="8d790-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="8d790-110">Utilidad de línea de comandos que se usa principalmente para registrar el proveedor en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8d790-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="8d790-111">También se puede utilizar para obtener información de metadatos sobre el proveedor, sus eventos y los canales en los que se registran los eventos, y para consultar los eventos de un canal o un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="8d790-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="8d790-112">La herramienta de WevtUtil.exe se incluye en% WINDIR% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="8d790-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="8d790-113">Para obtener información de uso, escriba "wevtutil/?"</span><span class="sxs-lookup"><span data-stu-id="8d790-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="8d790-114">en un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="8d790-114">at a command prompt.</span></span><br/> <span data-ttu-id="8d790-115">Este comando está limitado a los miembros del grupo administradores y debe ejecutarse con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="8d790-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
