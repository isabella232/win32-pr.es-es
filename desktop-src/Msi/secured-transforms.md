---
description: Las transformaciones protegidas a veces son necesarias por motivos de seguridad.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformaciones protegidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07c36b70827c301117bff7d98b30aae2990efb80f892bda24b0be35cbba5316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040845"
---
# <a name="secured-transforms"></a>Transformaciones protegidas

Las transformaciones protegidas a veces son necesarias por motivos de seguridad. Las transformaciones protegidas se almacenan localmente en el equipo del usuario en una ubicación donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Estas transformaciones se almacenan en caché en esta ubicación durante la instalación o el anuncio del paquete. Solo los administradores y el sistema local tienen acceso de escritura a esta ubicación. Un usuario que no es administrador no podría modificar el archivo de transformación. Durante las [instalaciones posteriores de instalación a petición](installation-on-demand.md) [o](maintenance-installation.md) de mantenimiento del paquete, el instalador usa las transformaciones almacenadas en caché.

Para especificar el almacenamiento de transformación protegido, establezca la directiva [TransformsSecure](transformssecure-policy.md), establezca la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o pase el símbolo @ o en \| la lista de transformaciones. Tenga en cuenta que no puede incluir transformaciones protegidas y no seguras en la misma lista de transformaciones. Vea [Aplicar transformaciones.](applying-transforms.md)

La eliminación del producto por parte de cualquier usuario quita todas las transformaciones protegidas para ese producto del equipo del usuario.

Si el instalador encuentra que una transformación protegida no está disponible localmente, intenta restaurar la caché de transformaciones desde un origen. Las transformaciones seguras pueden ser secure-at-source o secure-full-path:

-   [Las transformaciones seguras](secure-at-source-transforms.md) en el origen que faltan en la caché de transformación local se restauran desde la raíz del origen del archivo .msi origen.
-   [Las transformaciones de ruta de](secure-full-path-transforms.md) acceso completa segura que faltan en la caché de transformaciones local se restauran a partir de la ruta de acceso completa original especificada por la lista de transformaciones.

 

 



