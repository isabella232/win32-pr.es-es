---
description: Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que son demasiado pequeños para garantizar el cambio del código de producto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Actualizaciones pequeñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153873"
---
# <a name="small-updates"></a>Actualizaciones pequeñas

Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que son demasiado pequeños para garantizar el cambio del código de producto. También se suele hacer referencia a una actualización pequeña como una actualización de ingeniería de corrección rápida (QFE). Una actualización pequeña no permite la reorganización del árbol de componentes de características.

Una actualización pequeña típica solo cambia uno o dos archivos o una clave del registro. Dado que una actualización pequeña cambia la información en el archivo. msi, se debe cambiar el código del paquete de instalación. El código del paquete se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) de la secuencia de información de [Resumen](summary-information-stream.md).

El código de producto nunca cambia con una actualización pequeña, por lo que todos los cambios introducidos por una actualización pequeña deben ser coherentes con las directrices descritas en [cambiar el código de producto](changing-the-product-code.md). Una actualización requiere una [actualización importante](major-upgrades.md) para cambiar el [**ProductCode**](productcode.md). Si es necesario diferenciar los productos sin cambiar el código de producto, use una [actualización secundaria](minor-upgrades.md).

Para obtener información sobre cómo aplicar un pequeño paquete de revisión de actualización a un paquete de Windows Installer, consulte [crear una revisión de actualización pequeña](creating-a-small-update-patch.md), [aplicar actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)y [aplicar pequeñas actualizaciones mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md).

 

 



