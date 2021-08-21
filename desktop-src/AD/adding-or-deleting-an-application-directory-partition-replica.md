---
title: Agregar o eliminar una réplica de partición de directorio de aplicación
description: La primera réplica de una partición de directorio de aplicación se crea en el controlador de dominio que se enlazaba a ella en el momento de la creación.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Agregar o eliminar una réplica de partición de directorio de aplicación AD
- Application Directory Partitions AD , Agregar o eliminar una réplica de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adfc63012a6a153d2488e4d3353683ece2d611cb0b3e8e04794eaf76231ab61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024752"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Agregar o eliminar una réplica de partición de directorio de aplicación

La primera réplica de una partición de directorio de aplicación se crea en el controlador de dominio que se enlazaba a ella en el momento de la creación. Se pueden crear réplicas adicionales en cualquier controlador de dominio del bosque, no necesariamente en el mismo dominio que el controlador de dominio inicial. Una réplica de partición de directorio de aplicación solo puede existir en un controlador de dominio que ejecute Windows Server 2003 o posterior. Para más información, consulte este artículo de TechNet sobre administración [de particiones.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10))

**Para agregar una réplica para una partición de directorio de aplicación, realice los pasos siguientes:**

1.  Busque en el contenedor Partitions un [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición del directorio de la aplicación.
2.  Enlace al objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con la delegación habilitada. Esto es necesario porque el **objeto crossRef** solo se puede modificar en el Domain-Naming de roles FSMO. Con la delegación habilitada, el controlador de dominio puede ponerse en contacto Domain-Naming titular del rol FSMO con las mismas credenciales.
3.  Agregue el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio que hospedará la nueva réplica al atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef.**](/windows/desktop/ADSchema/c-crossref)

Cuando el nuevo valor del atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) se replica en el nuevo controlador de dominio que hospedará una réplica de la partición del directorio de la aplicación, el KCC se desencadenará para replicar la partición del directorio de la aplicación en el controlador de dominio de destino.

Para quitar una réplica de una partición de directorio de aplicación, realice los mismos pasos anteriores para buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de la aplicación y quitar el valor que corresponde al controlador de dominio del atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto **crossRef.**

Cuando el nuevo valor del atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) se replica en el controlador de dominio que ya no hospedará una réplica de la partición del directorio de la aplicación, el KCC se desencadenará para quitar la réplica de la partición del directorio de aplicación en el controlador de dominio de destino.

Si se quita o degrada un controlador de dominio que hospeda una réplica de partición de directorio de aplicación, el servidor de Active Directory quitará automáticamente el valor correspondiente al controlador de dominio del atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de todos los objetos [**crossRef.**](/windows/desktop/ADSchema/c-crossref)

 

 