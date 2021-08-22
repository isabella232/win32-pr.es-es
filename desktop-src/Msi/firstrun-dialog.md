---
description: Una secuencia de cuadro de diálogo FirstRun recopila información de nombre de usuario, nombre de empresa e identificador de producto. El instalador comprueba el identificador de producto durante este cuadro de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Cuadro de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de44417014aefb84d2d381166d5a2fceb7f956c4212e9dba31556053c583fef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828895"
---
# <a name="firstrun-dialog"></a>Cuadro de diálogo FirstRun

Una secuencia de cuadro de diálogo FirstRun recopila información de nombre de usuario, nombre de empresa e identificador de producto. El instalador comprueba el identificador de producto durante este cuadro de diálogo.

Normalmente, una secuencia de cuadro de diálogo FirstRun no forma parte de la secuencia de acciones y, en su lugar, la función [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) llama a ella en la primera ejecución del producto.

Un autor de un paquete de instalador puede usar la secuencia de diálogo de plantilla o crear una secuencia diferente. Sin embargo, la secuencia de diálogo debe hacer que el usuario establezca las siguientes propiedades:

-   [**Username, propiedad**](username.md)
-   [**COMPANYNAME,**](companyname.md) propiedad
-   [**PidKEY, propiedad**](pidkey.md)

El identificador de producto se validará durante el cuadro de diálogo mediante la [acción ValidateProductID](validateproductid-action.md) o [validateProductID ControlEvent](validateproductid-controlevent.md).

Si el identificador de producto se establece como una propiedad en la línea de comandos o mediante una transformación, la necesidad de que el usuario vuelva a escribir el identificador de producto durante el cuadro de diálogo de la primera ejecución se puede evitar controlando la presentación mediante la [**propiedad ProductID.**](productid.md) Después de la validación correcta del identificador de producto, la **propiedad ProductID** se establece en el identificador de producto completo y válido.

 

 



