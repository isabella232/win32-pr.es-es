---
description: Las transformaciones que no se han protegido como se describe en Transformaciones protegidas son transformaciones no seguras de forma predeterminada.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformaciones no seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bb234a0cdee852d3a5e1717642f5325283a571b740c9d7b4a5f6901afb52c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499615"
---
# <a name="unsecured-transforms"></a>Transformaciones no seguras

Las transformaciones que no se han protegido como se describe en [Transformaciones protegidas](secured-transforms.md) son transformaciones no seguras de forma predeterminada.

Para aplicar una transformación no segura al instalar un paquete, pase los nombres de archivo de transformación en la propiedad [**TRANSFORMS**](transforms.md) o la cadena de línea de comandos. No comience la cadena con los caracteres @ o ni establezca la directiva \| [TransformsSecure](transformssecure-policy.md) o la [**propiedad TRANSFORMSSECURE.**](transformssecure.md) Tenga en cuenta que no puede combinar transformaciones no seguras y [transformaciones protegidas](secured-transforms.md) en la misma lista de transformaciones.

Si el paquete se instala o anuncia [](installation-context.md)en el contexto de instalación por usuario y tiene transformaciones no seguras, el instalador guarda el origen de transformación en la carpeta Datos de la aplicación en el perfil del usuario. Esto permite que un usuario mantenga su personalización de un producto mientras se mueve entre equipos.

Si el paquete se instala o anuncia [](installation-context.md)en el contexto de instalación por equipo y usa transformaciones no seguras, el instalador guarda el origen de transformación en la carpeta %windir% \\ Installer.

Durante la primera instalación del paquete, el instalador busca primero la transformación en el origen proporcionado por la propiedad [**TRANSFORMS**](transforms.md) o la cadena de línea de comandos. Si este origen no está disponible, el instalador busca la transformación en el origen del paquete junto al .msi archivo.

Durante una [instalación de mantenimiento,](maintenance-installation.md)el instalador busca la transformación en la ubicación de caché. Si la copia almacenada en caché de la transformación deja de estar disponible, el instalador busca la transformación en el origen del paquete junto al .msi archivo.

Para obtener más información, [vea Aplicar transformaciones y](applying-transforms.md) resistencia de [origen.](source-resiliency.md)

 

 



