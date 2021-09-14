---
description: Una pequeña actualización realiza cambios en uno o varios archivos de aplicación que son demasiado menores para garantizar el cambio del código del producto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Actualizaciones pequeñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266111"
---
# <a name="small-updates"></a>Actualizaciones pequeñas

Una pequeña actualización realiza cambios en uno o varios archivos de aplicación que son demasiado menores para garantizar el cambio del código del producto. Una actualización pequeña también se conoce normalmente como actualización de ingeniería de corrección rápida (QFE). Una actualización pequeña no permite reorganizar el árbol de componentes de características.

Una actualización pequeña típica cambia solo uno o dos archivos o una clave del Registro. Dado que una pequeña actualización cambia la información del .msi, se debe cambiar el código del paquete de instalación. El código del paquete se almacena en la propiedad [**Resumen del**](revision-number-summary.md) número de revisión del flujo de información [de resumen](summary-information-stream.md).

El código del producto nunca cambia con una actualización pequeña, por lo que todos los cambios introducidos por una actualización pequeña deben ser coherentes con las directrices descritas en Cambio del código [de producto](changing-the-product-code.md). Una actualización requiere una [actualización principal para](major-upgrades.md) cambiar [**ProductCode**](productcode.md). Si es necesario diferenciar entre productos sin cambiar el código de producto, use una [actualización secundaria](minor-upgrades.md).

Para obtener información sobre cómo aplicar un pequeño paquete de revisión de actualización a un paquete del instalador de Windows, vea Crear una revisión de actualización [pequeña,](creating-a-small-update-patch.md)Aplicar pequeñas actualizaciones mediante la aplicación de revisiones a la instalación [local](applying-small-updates-by-patching-the-local-installation-of-the-product.md)del [producto,](applying-small-updates-by-reinstalling-the-product.md)Aplicar actualizaciones pequeñas reinstalando el producto y Aplicar pequeñas actualizaciones mediante la aplicación de revisiones a una [imagen administrativa.](applying-small-updates-by-patching-an-administrative-image.md)

 

 



