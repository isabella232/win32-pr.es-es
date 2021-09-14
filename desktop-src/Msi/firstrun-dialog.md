---
description: Una secuencia de cuadro de diálogo FirstRun recopila información de nombre de usuario, nombre de empresa e identificador de producto. El instalador comprueba el identificador de producto durante este cuadro de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Cuadro de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074774"
---
# <a name="firstrun-dialog"></a>Cuadro de diálogo FirstRun

Una secuencia de cuadro de diálogo FirstRun recopila información de nombre de usuario, nombre de empresa e identificador de producto. El instalador comprueba el identificador de producto durante este cuadro de diálogo.

Normalmente, una secuencia de cuadro de diálogo FirstRun no forma parte de la secuencia de acciones y, en su lugar, la función [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) llama a ella en la primera ejecución del producto.

Un autor de un paquete de instalador puede usar la secuencia de diálogo de plantilla o crear una secuencia diferente. Sin embargo, la secuencia de diálogo debe hacer que el usuario establezca las siguientes propiedades:

-   [**USERNAME, propiedad**](username.md)
-   [**Propiedad COMPANYNAME**](companyname.md)
-   [**Propiedad PIDKEY**](pidkey.md)

El identificador de producto se validará durante el cuadro de diálogo mediante la [acción ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent](validateproductid-controlevent.md).

Si el identificador de producto se establece como una propiedad en la línea de comandos o mediante una transformación, la necesidad de que el usuario vuelva a escribir el identificador de producto durante el cuadro de diálogo de primera ejecución se puede sortear mediante el control de la presentación mediante la [**propiedad ProductID.**](productid.md) Después de la validación correcta del identificador de producto, la **propiedad ProductID** se establece en el identificador de producto completo y válido.

 

 



