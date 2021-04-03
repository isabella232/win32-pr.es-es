---
title: BITS y restauración del sistema
description: No todas las versiones de BITS usan el mismo formato para almacenar los trabajos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075262"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="27960-103">BITS y restauración del sistema</span><span class="sxs-lookup"><span data-stu-id="27960-103">BITS and System Restore</span></span>

<span data-ttu-id="27960-104">No todas las versiones de BITS usan el mismo formato para almacenar los trabajos.</span><span class="sxs-lookup"><span data-stu-id="27960-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="27960-105">Si devuelve el equipo a un punto de restauración antes de una actualización de BITS, es posible que la versión anterior de BITS no pueda leer la información del trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="27960-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="27960-106">Si esto ocurre, BITS eliminará la lista de trabajos y creará una nueva lista de trabajos vacía.</span><span class="sxs-lookup"><span data-stu-id="27960-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="27960-107">Como resultado, los archivos temporales asociados a la lista de trabajos anteriores no se limpian; para recuperar el espacio en disco, debe eliminar manualmente los archivos.</span><span class="sxs-lookup"><span data-stu-id="27960-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="27960-108">Los usuarios familiarizados con la línea de comandos de Windows pueden evitar este problema mediante la [herramienta BITSAdmin](bitsadmin-tool.md) para borrar la lista de trabajos de bits antes de ejecutar Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="27960-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="27960-109">Para borrar la lista de trabajos de BITS, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="27960-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="27960-110">**bitsadmin/RESET/AllUsers**</span><span class="sxs-lookup"><span data-stu-id="27960-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="27960-111">Tenga en cuenta que debe tener privilegios de administrador para ejecutar este comando.</span><span class="sxs-lookup"><span data-stu-id="27960-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




