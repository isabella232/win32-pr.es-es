---
description: En este ejemplo se muestra cómo crear un paquete de revisión que aplica una pequeña actualización al paquete de instalación de ejemplo que se describe en un ejemplo de instalación.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Un pequeño ejemplo de revisión de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667072"
---
# <a name="a-small-update-patching-example"></a>Un pequeño ejemplo de revisión de actualización

En este ejemplo se muestra cómo crear un [paquete de revisión](patch-packages.md) que aplica una [pequeña actualización](small-updates.md) al paquete de instalación de ejemplo que se describe en [un ejemplo de instalación](an-installation-example.md). Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que se consideran demasiado pequeños para garantizar el cambio del código de producto. Para obtener más información [, consulte revisiones y actualizaciones](patching-and-upgrades.md).

En este ejemplo se muestra cómo crear un paquete de revisión de Windows Installer que actualiza la característica de concierto de la MNP2000 de producto hipotética para corregir un error en el producto original. El paquete de revisión de ejemplo aplica una pequeña actualización al producto que no requiere cambiar el código de producto. Consulte el tema sobre las [actualizaciones principales](major-upgrades.md) en la sección [revisiones y actualizaciones](patching-and-upgrades.md) para obtener más información sobre las actualizaciones principales.

El paquete de actualización de ejemplo tiene las siguientes especificaciones:

-   Corrige un error leve en la programación del concierto que muestra la característica de concierto.
-   Actualiza el código de paquete para reflejar que el paquete de instalación ha cambiado.
-   La actualización pequeña se puede aplicar revisando la instalación local del producto.

[Continuar](planning-a-small-update-patch.md)

 

 



