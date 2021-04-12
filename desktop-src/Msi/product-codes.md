---
description: El código de producto es un GUID que es la identificación principal de una aplicación o producto.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Códigos de producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278274"
---
# <a name="product-codes"></a>Códigos de producto

El código de producto es un GUID que es la identificación principal de una aplicación o producto. Para obtener más información, vea la propiedad [**ProductCode**](productcode.md) . Si se realizan cambios significativos en un producto, el código de producto también debe cambiarse para reflejarlo. No obstante, no es necesario cambiar el código de producto si los cambios en el producto son relativamente pequeños.

Las versiones de 32 bits y 64 bits del paquete de una aplicación deben tener distintos códigos de producto. Si cualquier componente de 32 bits de una aplicación se vuelve a compilar en un componente de 64 bits, se debe asignar un nuevo código de producto.

Si un servidor expuesto en la [tabla PublishComponent](publishcomponent-table.md) se vuelve a compilar de 32 bits a 64 bits, es posible que también sea necesario cambiar el GUID de esta tabla para que los clientes de 32 y 64 bits puedan identificar la categoría de componente cualificada adecuada. En este caso, también se debe cambiar el código de producto.

Tenga en cuenta que las letras de los GUID de código de producto deben estar en mayúsculas. Las utilidades como GUIDGEN generan GUID que contienen letras minúsculas. Las letras minúsculas de estos GUID deben cambiarse a mayúsculas para usarse como código de producto o código de paquete. Para obtener más información, consulte [cambiar el código de producto](changing-the-product-code.md).

El código del paquete es un GUID que identifica un [*paquete*](p-gly.md)de Windows Installer determinado. El código del paquete asocia un archivo. msi a una aplicación o un producto y también se puede usar para la comprobación de orígenes. Los códigos de producto y paquete no son intercambiables. Dos archivos. msi no idénticos deben tener el mismo código de paquete. Aunque es habitual enviar una aplicación que tenga el mismo código de paquete y el mismo código de producto, los dos valores pueden diferir a medida que se actualiza la aplicación. Para obtener más información, consulte [códigos de paquete](package-codes.md).

 

 



