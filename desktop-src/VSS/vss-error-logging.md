---
description: 'La siguiente información de error y estado de VSS se escribe en el registro de eventos de la aplicación:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registro de errores de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154336"
---
# <a name="vss-error-logging"></a>Registro de errores de VSS

La siguiente información de error y estado de VSS se escribe en el registro de eventos de la aplicación:

-   Errores del solicitante generados mediante la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Los errores de escritura producidos en mediante la clase [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , incluidos los métodos de invalidación
-   Errores generados por el proveedor predeterminado
-   Errores del servicio VSS generados en la coordinación de la actividad de proveedor, escritor y solicitante (por ejemplo, la generación de eventos)

Estos errores pueden tener varias causas, incluido un error de programación en código de terceros o errores de configuración relacionados con VSS.

Los controladores VSS y la funcionalidad de implementación de nivel inferior escriben errores en el registro del sistema. El software de terceros (solicitante, proveedor, redactor) puede elegir el registro de la aplicación, el registro del sistema, o ambos, para escribir entradas del registro de errores.

Se recomienda que las aplicaciones de alto nivel (como el código en modo de usuario) utilicen el registro de aplicaciones. Las aplicaciones de nivel inferior, como las interfaces de hardware y los controladores, deben utilizar el registro del sistema.

 

 



