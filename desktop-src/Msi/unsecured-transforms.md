---
description: Las transformaciones que no se han protegido tal y como se describe en transformaciones protegidas son transformaciones no seguras de forma predeterminada.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformaciones no seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678523"
---
# <a name="unsecured-transforms"></a>Transformaciones no seguras

Las transformaciones que no se han protegido tal y como se describe en [transformaciones protegidas](secured-transforms.md) son transformaciones no seguras de forma predeterminada.

Para aplicar una transformación no segura al instalar un paquete, pase los nombres de archivo de transformación en la propiedad de [**TRANSformaciones**](transforms.md) o en la cadena de línea de comandos. No empiece la cadena con los caracteres @ o \| o establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) . Tenga en cuenta que no se pueden combinar transformaciones no seguras y [transformaciones protegidas](secured-transforms.md) en la misma lista de transformaciones.

Si el paquete se instala o se anuncia en el [contexto de instalación](installation-context.md)por usuario y tiene transformaciones no seguras, el instalador guarda el origen de la transformación en la carpeta datos de la aplicación en el perfil del usuario. Esto permite al usuario mantener su personalización de un producto mientras se mueve entre equipos.

Si el paquete se instala o se anuncia en el [contexto de instalación](installation-context.md)por equipo y usa transformaciones no seguras, el instalador guarda el origen de transformación en la carpeta% WINDIR% \\ Installer.

Durante una instalación del paquete por primera vez, el instalador busca primero la transformación en el origen proporcionado por la propiedad [**TRANSformation**](transforms.md) o la cadena de línea de comandos. Si el origen no está disponible, el instalador busca la transformación en el origen del paquete situado junto al archivo. msi.

Durante una [instalación de mantenimiento](maintenance-installation.md), el instalador busca la transformación en la ubicación de la memoria caché. Si la copia almacenada en caché de la transformación deja de estar disponible, el instalador busca la transformación en el origen del paquete situado junto al archivo. msi.

Para obtener más información, vea [aplicar transformaciones](applying-transforms.md) y [resistencia de origen](source-resiliency.md).

 

 



