---
description: En este ejemplo se muestra cómo crear un paquete de revisión que aplica una pequeña actualización al paquete de instalación de ejemplo que se describe en Un ejemplo de instalación.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Ejemplo de aplicación de revisiones de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082975"
---
# <a name="a-small-update-patching-example"></a>Ejemplo de aplicación de revisiones de actualización pequeña

En este ejemplo se muestra cómo crear un [paquete](patch-packages.md) de revisión que aplica [una](small-updates.md) pequeña actualización al paquete de instalación de ejemplo que se describe en [Un ejemplo de instalación](an-installation-example.md). Una pequeña actualización realiza cambios en uno o varios archivos de aplicación que se considera demasiado menores para garantizar el cambio del código del producto. Para obtener más información, [vea Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)

En este ejemplo se muestra cómo crear un paquete de revisión de Windows Installer que actualiza la característica Concert del producto hipotético MNP2000 para corregir un error en el producto original. El paquete de revisión de ejemplo aplica una pequeña actualización al producto que no requiere cambiar el código del producto. Vea el tema Actualizaciones [principales en](major-upgrades.md) la sección [Revisiones](patching-and-upgrades.md) y actualizaciones para obtener más información sobre las actualizaciones principales.

El paquete de actualización de ejemplo tiene las especificaciones siguientes:

-   Corrige un error menor en la programación de concerto que muestra la característica Concert.
-   Actualiza el código del paquete para reflejar que el paquete de instalación ha cambiado.
-   La pequeña actualización se puede aplicar mediante la aplicación de revisiones a la instalación local del producto.

[Continuar](planning-a-small-update-patch.md)

 

 



