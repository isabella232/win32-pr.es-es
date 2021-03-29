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
# <a name="using-the-file-log"></a>Uso del registro de archivos

Antes de poder usar un registro de archivos, debe llamar a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) para abrirlo o crearlo. Cuando se llama a esta función, puede especificar marcas para crear o sobrescribir un registro de archivos, abrir el registro del sistema o abrir un registro de archivos como de solo lectura.

Una vez que [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) devuelve un identificador a un registro de archivos, puede Agregar una entrada mediante una llamada a [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), eliminar una entrada llamando a [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)o recuperar información sobre un archivo determinado en un registro de archivos llamando a [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).

Cuando el registro de archivos ya no se necesita, se debe llamar a [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) para liberar los recursos asignados durante la llamada a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).

 

 



