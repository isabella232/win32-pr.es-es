---
description: En este ejemplo se muestra cómo crear un paquete de revisión que aplica una pequeña actualización al paquete de instalación de ejemplo que se describe en Un ejemplo de instalación.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Ejemplo pequeño de aplicación de revisiones de actualizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159271"
---
# <a name="a-small-update-patching-example"></a>Ejemplo pequeño de aplicación de revisiones de actualizaciones

En este ejemplo se muestra cómo crear un [paquete](patch-packages.md) de revisión que aplica una pequeña actualización [al](small-updates.md) paquete de instalación de ejemplo que se describe en [Un ejemplo de instalación](an-installation-example.md). Una pequeña actualización realiza cambios en uno o varios archivos de aplicación que se considera demasiado menores para garantizar el cambio del código del producto. Para obtener más información, [vea Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)

En este ejemplo se muestra cómo crear un paquete de revisión del instalador de Windows que actualiza la característica Concert del producto hipotético MNP2000 para corregir un error en el producto original. El paquete de revisión de ejemplo aplica una pequeña actualización al producto que no requiere cambiar el código del producto. Vea el tema actualizaciones [principales en](major-upgrades.md) la sección [Revisiones](patching-and-upgrades.md) y actualizaciones para obtener más información sobre las actualizaciones principales.

El paquete de actualización de ejemplo tiene las siguientes especificaciones:

-   Corrige un error menor en la programación del concertado mostrada por la característica Concert.
-   Actualiza el código del paquete para reflejar que el paquete de instalación ha cambiado.
-   La pequeña actualización se puede aplicar mediante la aplicación de revisiones a la instalación local del producto.

[Continuar](planning-a-small-update-patch.md)

 

 



