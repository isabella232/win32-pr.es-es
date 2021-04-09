---
title: Agregar o eliminar una réplica de partición de directorio de aplicaciones
description: La primera réplica de una partición de directorio de aplicaciones se crea en el controlador de dominio que estaba enlazada en el momento de la creación.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Agregar o eliminar un AD de réplica de partición de directorio de aplicaciones
- Particiones de directorio de aplicaciones AD, agregar o eliminar una réplica de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149185"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Agregar o eliminar una réplica de partición de directorio de aplicaciones

La primera réplica de una partición de directorio de aplicaciones se crea en el controlador de dominio que estaba enlazada en el momento de la creación. Se pueden crear réplicas adicionales en cualquier controlador de dominio del bosque, no necesariamente en el mismo dominio que el controlador de dominio inicial. Una réplica de partición de directorio de aplicaciones solo puede existir en un controlador de dominio que ejecute Windows Server 2003 o posterior. Para obtener más información, consulte este artículo de TechNet sobre la [Administración de particiones](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Para agregar una réplica para una partición de directorio de aplicaciones, siga estos pasos:**

1.  Busque en el contenedor de particiones un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición de directorio de aplicaciones.
2.  Enlazar al objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con la delegación habilitada. Esto es necesario porque el objeto **crossRef** solo puede modificarse en el titular de la función FSMO Domain-Naming. Con la delegación habilitada, el controlador de dominio puede ponerse en contacto con el titular de la función FSMO de Domain-Naming con las mismas credenciales.
3.  Agregue el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio que va a hospedar la nueva réplica en el atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Cuando el nuevo valor del atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) se replica en el nuevo controlador de dominio que hospedará una réplica de la partición de directorio de aplicaciones, el KCC se desencadenará para replicar la partición de directorio de aplicaciones en el controlador de dominio de destino.

Para quitar una réplica de una partición de directorio de aplicaciones, realice los mismos pasos anteriores para buscar el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa la partición del directorio de la aplicación y quitar el valor que corresponde al controlador de dominio del atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto **crossRef** .

Cuando el nuevo valor del atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) se replique en el controlador de dominio que ya no hospedará una réplica de la partición de directorio de aplicaciones, el KCC se desencadenará para quitar la réplica de la partición de directorio de aplicaciones en el controlador de dominio de destino.

Si se quita o se degrada un controlador de dominio que hospeda una réplica de partición de directorio de aplicaciones, el servidor de Active Directory quitará automáticamente el valor correspondiente al controlador de dominio del atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de todos los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

 

 