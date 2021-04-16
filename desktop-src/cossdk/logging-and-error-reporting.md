---
description: Registro e informes de errores
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registro e informes de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677237"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="b5c46-103">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="b5c46-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="b5c46-104">Archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b5c46-104">Log file</span></span>

<span data-ttu-id="b5c46-105">COMREPL genera un archivo de registro que contiene mensajes de estado y de error.</span><span class="sxs-lookup"><span data-stu-id="b5c46-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="b5c46-106">Este archivo se almacena en el equipo en el que se inició COMREPL en% systemdir% \\ com \\ replicate \\ COMRepl. log.</span><span class="sxs-lookup"><span data-stu-id="b5c46-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="b5c46-107">Este archivo de registro se borra cuando se inicia una fase de copia.</span><span class="sxs-lookup"><span data-stu-id="b5c46-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="b5c46-108">La instalación posterior en destinos se anexará al archivo.</span><span class="sxs-lookup"><span data-stu-id="b5c46-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="b5c46-109">Control de errores</span><span class="sxs-lookup"><span data-stu-id="b5c46-109">Error handling</span></span>

<span data-ttu-id="b5c46-110">Los errores se indican en el archivo de registro que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b5c46-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="b5c46-111">También se puede encontrar información detallada del error en el registro de eventos de los equipos de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="b5c46-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5c46-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5c46-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c46-113">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="b5c46-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="b5c46-114">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="b5c46-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="b5c46-115">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="b5c46-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="b5c46-116">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="b5c46-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



