---
description: Una actualización secundaria es una actualización que realiza cambios en muchos recursos.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Actualizaciones secundarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911905"
---
# <a name="minor-upgrades"></a>Actualizaciones secundarias

Una actualización secundaria es una actualización que realiza cambios en muchos recursos. Ninguno de los cambios puede requerir el cambio de [**ProductCode**](productcode.md). Una actualización requiere una [actualización importante](major-upgrades.md) para cambiar el **ProductCode**. Una actualización secundaria se puede usar para agregar nuevas características y componentes, pero no puede reorganizar el árbol de componentes de características. Las actualizaciones secundarias proporcionan diferenciación del producto sin definir realmente un producto diferente. Una actualización secundaria típica incluye todas las correcciones de las actualizaciones pequeñas anteriores combinadas en una revisión. Una actualización secundaria también se conoce normalmente como una actualización de Service Pack (SP). Para obtener más información acerca de las actualizaciones que no requieren el cambio de **ProductCode** , consulte [cambiar el código de producto](changing-the-product-code.md).

Una actualización secundaria cambia la propiedad [**ProductVersion**](productversion.md) . El cambio de la versión del producto de la aplicación significa que las diferentes actualizaciones tienen un pedido. Por ejemplo, si existiera una revisión para actualizar v 9,0 a v 9,1 y existiera otra revisión para la revisión v 9,1 a v 9,2, el instalador puede aplicar el orden correcto comprobando la versión del producto antes de aplicar la revisión. Esto también impide que la revisión v 9,1 a v 9,2 se aplique a v 9,0. En el caso de las revisiones, este orden se aplica a través de la versión del producto: bits de validación establecidos en las transformaciones incluidas en el [paquete de revisión](patch-packages.md).

Una actualización secundaria y una pequeña actualización difieren en que una actualización secundaria cambia el código de paquete y la versión del producto. Vea [actualizaciones pequeñas](small-updates.md) para obtener instrucciones sobre los tipos de actualizaciones que se pueden administrar mediante una pequeña actualización o una actualización secundaria. Las actualizaciones secundarias se envían como un paquete de instalación de producto completo o como un [paquete de revisión](patch-packages.md). Sin embargo, una actualización secundaria no puede usar una etiqueta de volumen diferente para la nueva versión.

Para obtener información sobre cómo aplicar una actualización secundaria, vea los temas siguientes:

-   [Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)
-   [Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)

 

 



