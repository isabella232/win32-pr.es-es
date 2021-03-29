---
description: Antes de poder usar un registro de archivos, debe llamar a SetupInitializeFileLog para abrirlo o crearlo. Cuando se llama a esta función, puede especificar marcas para crear o sobrescribir un registro de archivos, abrir el registro del sistema o abrir un registro de archivos como de solo lectura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Uso del registro de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003212"
---
# <a name="using-the-file-log"></a><span data-ttu-id="b0927-104">Uso del registro de archivos</span><span class="sxs-lookup"><span data-stu-id="b0927-104">Using the File Log</span></span>

<span data-ttu-id="b0927-105">Antes de poder usar un registro de archivos, debe llamar a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) para abrirlo o crearlo.</span><span class="sxs-lookup"><span data-stu-id="b0927-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="b0927-106">Cuando se llama a esta función, puede especificar marcas para crear o sobrescribir un registro de archivos, abrir el registro del sistema o abrir un registro de archivos como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b0927-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="b0927-107">Una vez que [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) devuelve un identificador a un registro de archivos, puede Agregar una entrada mediante una llamada a [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), eliminar una entrada llamando a [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)o recuperar información sobre un archivo determinado en un registro de archivos llamando a [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span><span class="sxs-lookup"><span data-stu-id="b0927-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="b0927-108">Cuando el registro de archivos ya no se necesita, se debe llamar a [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) para liberar los recursos asignados durante la llamada a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span><span class="sxs-lookup"><span data-stu-id="b0927-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



