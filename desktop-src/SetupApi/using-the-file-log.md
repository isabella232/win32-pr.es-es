---
description: Para poder usar un registro de archivos, debe llamar a SetupInitializeFileLog para abrirlo o crearlo. Al llamar a esta función, puede especificar marcas para crear o sobrescribir un registro de archivos, abrir el registro del sistema o abrir un registro de archivos como de solo lectura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Uso del registro de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39772a668f3e0920df6f7f023ed481de5f9676954b276625335772220eab385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963913"
---
# <a name="using-the-file-log"></a>Uso del registro de archivos

Para poder usar un registro de archivos, debe llamar a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) para abrirlo o crearlo. Al llamar a esta función, puede especificar marcas para crear o sobrescribir un registro de archivos, abrir el registro del sistema o abrir un registro de archivos como de solo lectura.

Después de que [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) devuelva un identificador a un registro de archivos, puede agregar una entrada llamando a [**SetupLogFile,**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)eliminar una entrada mediante una llamada a [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)o recuperar información sobre un archivo determinado en un registro de archivos mediante una llamada a [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).

Cuando ya no se necesite el registro de archivos, se debe llamar a [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) para liberar los recursos asignados durante la llamada a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).

 

 



