---
description: Las transformaciones protegidas a veces son necesarias por motivos de seguridad.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformaciones protegidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913658"
---
# <a name="secured-transforms"></a>Transformaciones protegidas

Las transformaciones protegidas a veces son necesarias por motivos de seguridad. Las transformaciones protegidas se almacenan localmente en el equipo del usuario en una ubicación en la que, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Dichas transformaciones se almacenan en caché en esta ubicación durante la instalación o el anuncio del paquete. Solo los administradores y el sistema local tienen acceso de escritura a esta ubicación. Un usuario que no sea administrador no podrá modificar el archivo de transformación. Durante la [instalación](installation-on-demand.md) posterior a petición o las [instalaciones de mantenimiento](maintenance-installation.md) del paquete, el instalador usa las transformaciones almacenadas en caché.

Para especificar el almacenamiento de transformación seguro, establezca la [Directiva TransformsSecure](transformssecure-policy.md), establezca la propiedad [**TransformsSecure**](transformssecure.md) o pase el símbolo @ o \| en la lista transformaciones. Tenga en cuenta que no puede incluir transformaciones seguras y no seguras en la misma lista de transformaciones. Consulte [aplicar transformaciones](applying-transforms.md).

La eliminación del producto por cualquier usuario quita todas las transformaciones protegidas de ese producto del equipo del usuario.

Si el instalador detecta que una transformación protegida no está disponible localmente, intenta restaurar la memoria caché de transformación desde un origen. Las transformaciones seguras pueden ser seguras en el origen o en una ruta de acceso completa:

-   Las [transformaciones seguras en el origen](secure-at-source-transforms.md) que faltan en la memoria caché de transformación local se restauran desde la raíz del origen del archivo. msi.
-   Las [transformaciones de ruta de acceso completas seguras](secure-full-path-transforms.md) que faltan en la memoria caché de transformación local se restauran desde la ruta de acceso completa original especificada por la lista de transformaciones.

 

 



