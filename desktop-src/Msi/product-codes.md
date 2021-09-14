---
description: El código de producto es un GUID que es la identificación principal de una aplicación o producto.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Códigos de producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161436"
---
# <a name="product-codes"></a>Códigos de producto

El código de producto es un GUID que es la identificación principal de una aplicación o producto. Para obtener más información, vea la [**propiedad ProductCode.**](productcode.md) Si se realizan cambios significativos en un producto, el código del producto también debe cambiarse para reflejarlo. Sin embargo, no es necesario cambiar el código del producto si los cambios realizados en el producto son relativamente menores.

Las versiones de 32 y 64 bits del paquete de una aplicación deben tener códigos de producto diferentes. Si algún componente de 32 bits de una aplicación se vuelve a compilar en un componente de 64 bits, se debe asignar un nuevo código de producto.

Si se vuelve a compilar un servidor expuesto en la tabla [PublishComponent](publishcomponent-table.md) de 32 bits a 64 bits, es posible que también sea necesario cambiar el GUID de esta tabla para que los clientes de 32 bits y 64 bits puedan identificar la categoría de componente calificado adecuada. En este caso, también se debe cambiar el código del producto.

Tenga en cuenta que las letras de los GUID del código de producto deben estar en mayúsculas. Utilidades como GUIDGEN generan GUID que contienen letras minúsculas. Las letras minúsculas de estos GUID deben cambiarse a mayúsculas para que se utilicen como código de producto o código de paquete. Para obtener más información, vea [Cambiar el código de producto](changing-the-product-code.md).

El código del paquete es un GUID que identifica una Windows paquete del [*instalador.*](p-gly.md) El código del paquete asocia un .msi a una aplicación o producto y también se puede usar para la comprobación de orígenes. Los códigos de producto y paquete no son intercambiables. Dos archivos de .msi no identificados nunca deben tener el mismo código de paquete. Aunque es habitual enviar una aplicación que tiene el mismo código de paquete y código de producto, los dos valores pueden divergen a medida que se actualiza la aplicación. Para obtener más información, vea [Códigos de paquete](package-codes.md).

 

 



