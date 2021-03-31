---
description: Usar COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Usar COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807628"
---
# <a name="using-comrepl"></a><span data-ttu-id="7f697-103">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="7f697-103">Using COMREPL</span></span>

<span data-ttu-id="7f697-104">Para iniciar la utilidad de línea de comandos COMREPL, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="7f697-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="7f697-105">Agregue% WINDIR% \\ system32 \\ com a la ruta de acceso predeterminada del entorno; para ello, escriba lo siguiente en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="7f697-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="7f697-106">**establecer ruta de acceso =% PATH%;% WINDIR% \\ system32 \\ com**</span><span class="sxs-lookup"><span data-stu-id="7f697-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="7f697-107">Escriba el siguiente comando de COMREPL:</span><span class="sxs-lookup"><span data-stu-id="7f697-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="7f697-108">**COMREPL** *es sourcecomputer,* *targetComputerList* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="7f697-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="7f697-109">donde:</span><span class="sxs-lookup"><span data-stu-id="7f697-109">where:</span></span>

    -   <span data-ttu-id="7f697-110">*es sourcecomputer,* es el nombre de equipo del origen.</span><span class="sxs-lookup"><span data-stu-id="7f697-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="7f697-111">*targetComputerList* son los nombres de equipo de los destinos separados por espacios</span><span class="sxs-lookup"><span data-stu-id="7f697-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="7f697-112">**/n** suprime la solicitud de confirmación antes de iniciar la replicación</span><span class="sxs-lookup"><span data-stu-id="7f697-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="7f697-113">**/v** muestra la salida del archivo de registro en la consola</span><span class="sxs-lookup"><span data-stu-id="7f697-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="7f697-114">Notas</span><span class="sxs-lookup"><span data-stu-id="7f697-114">Notes</span></span>

-   <span data-ttu-id="7f697-115">Dado que no se replica COM+ (solo los datos y las aplicaciones de configuración), todos los equipos de destino deben tener instalado COM+.</span><span class="sxs-lookup"><span data-stu-id="7f697-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="7f697-116">El usuario debe pasar las comprobaciones de roles para la aplicación del sistema en los equipos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="7f697-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="7f697-117">No se replican las cuentas de equipo local que puedan usar los roles.</span><span class="sxs-lookup"><span data-stu-id="7f697-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="7f697-118">Los equipos de destino deben estar en línea.</span><span class="sxs-lookup"><span data-stu-id="7f697-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="7f697-119">El usuario es responsable de replicar todos los datos que no son COM (por ejemplo, tablas de base de datos, archivos de datos, etc.) en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="7f697-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="7f697-120">Los clústeres pueden participar en la replicación, pero tenga en cuenta que COMREPL solo se replica en equipos con nombre.</span><span class="sxs-lookup"><span data-stu-id="7f697-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f697-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f697-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f697-122">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="7f697-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="7f697-123">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="7f697-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="7f697-124">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="7f697-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="7f697-125">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="7f697-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



