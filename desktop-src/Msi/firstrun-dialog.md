---
description: Una secuencia del cuadro de diálogo FirstRun recopila información sobre el nombre de usuario, el nombre de la compañía y el ID. del producto. El instalador comprueba el ID. de producto durante este cuadro de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Cuadro de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275930"
---
# <a name="firstrun-dialog"></a>Cuadro de diálogo FirstRun

Una secuencia del cuadro de diálogo FirstRun recopila información sobre el nombre de usuario, el nombre de la compañía y el ID. del producto. El instalador comprueba el ID. de producto durante este cuadro de diálogo.

Normalmente, una secuencia del cuadro de diálogo FirstRun no forma parte de la secuencia de acción y, en su lugar, la llama la función [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) en la primera ejecución del producto.

Un autor de un paquete del instalador puede usar la secuencia del cuadro de diálogo de plantilla o crear una secuencia diferente. Sin embargo, la secuencia de diálogo necesita que el usuario establezca las siguientes propiedades:

-   Propiedad [**username**](username.md)
-   Propiedad [**CompanyName**](companyname.md)
-   Propiedad [**PIDKEY**](pidkey.md)

El identificador de producto se validará durante el diálogo con la [Acción ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent,](validateproductid-controlevent.md).

Si el ID. del producto se establece como una propiedad en la línea de comandos o mediante una transformación, la necesidad de que el usuario vuelva a escribir el ID. de producto durante el primer cuadro de diálogo de ejecución se puede eludir controlando la presentación mediante la propiedad [**ProductID**](productid.md) . Tras la validación correcta del ID. del producto, la propiedad **ProductID** se establece en el identificador de producto válido completo.

 

 



