---
description: 'La siguiente información de estado y error de VSS se escribe en el registro de eventos de aplicación:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registro de errores de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c2743fc6c23458a1059287a7731777e92447e3cd57ebf52e40baf7619c5658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056233"
---
# <a name="vss-error-logging"></a>Registro de errores de VSS

La siguiente información de estado y error de VSS se escribe en el registro de eventos de aplicación:

-   Errores del solicitante generados mediante la [**interfaz IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Errores de escritor producidos en el uso de [**la clase CVssWriter,**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) incluidos los métodos de invalidación
-   Errores generados por el proveedor predeterminado
-   Errores de servicio de VSS generados en la coordinación de la actividad del proveedor, escritor y solicitante (por ejemplo, la generación de eventos)

Estos errores pueden tener varias causas, incluido un error de programación en código de terceros o errores de configuración relacionados con VSS.

Los controladores de VSS y la funcionalidad de implementación de nivel inferior escriben errores en el registro del sistema. El software de terceros (solicitante, proveedor, escritor) puede elegir el registro de aplicación, el registro del sistema o ambos para escribir entradas del registro de errores.

Se recomienda que las aplicaciones de alto nivel (como el código en modo de usuario) usen el registro de aplicaciones. Las aplicaciones de nivel inferior, como las interfaces de hardware y los controladores, deben usar el registro del sistema.

 

 



