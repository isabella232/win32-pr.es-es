---
title: Referencia de restauración del sistema heredada
description: En esta documentación se describen los detalles de implementación del repositorio que usa una versión heredada de restaurar sistema. No se aplica a la implementación de restaurar sistema en Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903131"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="f093e-104">Referencia de restauración del sistema heredada</span><span class="sxs-lookup"><span data-stu-id="f093e-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="f093e-105">\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="f093e-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="f093e-106">En esta documentación se describen los detalles de implementación del repositorio que usa una versión heredada de restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="f093e-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="f093e-107">No se aplica a la implementación de restaurar sistema en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f093e-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="f093e-108">Estructura del repositorio de restauración del sistema</span><span class="sxs-lookup"><span data-stu-id="f093e-108">System Restore Repository Structure</span></span>

<span data-ttu-id="f093e-109">Windows XP con SP2 contiene un repositorio para restaurar el sistema en la siguiente carpeta:% SYSTEMDRIVE% \\ información del volumen del sistema.</span><span class="sxs-lookup"><span data-stu-id="f093e-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="f093e-110">Este repositorio contiene información sobre los puntos de restauración, que son básicamente una instantánea del sistema en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="f093e-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="f093e-111">El repositorio está estructurado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="f093e-111">The repository is structured as follows:</span></span>

<span data-ttu-id="f093e-112">**Restaurar información de volumen del sistema**    \*\* \_ {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="f093e-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="f093e-113">Para determinar qué \_ carpeta de restauración {*GUID*} usar, lea el **GUID** especificado en el siguiente archivo: raízdelsistema% \\ system32 \\ restore \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="f093e-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="f093e-114">Dentro de cada \_ carpeta restore {*GUID*}, el \_ archivo driver. cfg contiene información de una estructura de **\_ \_ configuración persistente de Sr** definida como sigue:</span><span class="sxs-lookup"><span data-stu-id="f093e-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="f093e-115">Archivos contenidos en cada carpeta RP *n*</span><span class="sxs-lookup"><span data-stu-id="f093e-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="f093e-116">Cada carpeta RP *n* contiene una carpeta de instantáneas que contiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f093e-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="f093e-117">Una instantánea de los subárboles del registro</span><span class="sxs-lookup"><span data-stu-id="f093e-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="f093e-118">Una carpeta de repositorio que contiene una instantánea del repositorio WMI</span><span class="sxs-lookup"><span data-stu-id="f093e-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="f093e-119">Una instantánea de la base de datos de COM+</span><span class="sxs-lookup"><span data-stu-id="f093e-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="f093e-120">Una instantánea de la base de datos de IIS</span><span class="sxs-lookup"><span data-stu-id="f093e-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="f093e-121">Cada carpeta RP *n* contiene un archivo RP. log que contiene información general sobre el punto de restauración de la estructura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f093e-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="f093e-122">Cada carpeta RP *n* puede contener archivos usados para realizar el seguimiento de los cambios de un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="f093e-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="f093e-123">El primer archivo se denomina Change. log, el siguiente archivo se denomina Change. log. 1, etc.</span><span class="sxs-lookup"><span data-stu-id="f093e-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="f093e-124">Cada archivo de registro de cambios contiene las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f093e-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="f093e-125">**\_encabezado de registro de cambios \_**</span><span class="sxs-lookup"><span data-stu-id="f093e-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="f093e-126">[**Cambiar \_ \_Entrada de registro**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="f093e-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="f093e-127">[**Cambiar \_ \_Entrada de registro**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="f093e-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="f093e-128">...</span><span class="sxs-lookup"><span data-stu-id="f093e-128">...</span></span>
-   <span data-ttu-id="f093e-129">[**Cambiar \_ \_Entrada de registro**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="f093e-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="f093e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f093e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f093e-131">Estructuras de restauración del sistema heredadas</span><span class="sxs-lookup"><span data-stu-id="f093e-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




