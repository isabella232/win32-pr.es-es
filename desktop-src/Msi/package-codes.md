---
description: El código del paquete es un GUID que identifica un paquete Windows installer.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Códigos de paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c49849ea3d441bba69fa05f549ee6f2f0d0d8560802235d5c18834f026d6c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145478"
---
# <a name="package-codes"></a>Códigos de paquete

El código del paquete es un GUID que identifica una Windows paquete del [*instalador.*](p-gly.md) El código del paquete asocia un .msi a una aplicación o producto y también se puede usar para la comprobación de orígenes. Los códigos de producto y paquete no son intercambiables. Para obtener más información, vea [Códigos de producto.](product-codes.md)

Los archivos .msi noidenticales no deben tener el mismo código de paquete. Es importante cambiar el código del paquete porque es el identificador principal que usa el instalador para buscar y validar el paquete correcto para una instalación determinada. Si se cambia un paquete sin cambiar el código del paquete, es posible que el instalador no use el paquete más reciente si ambos siguen siendo accesibles para el instalador.

El código del paquete se almacena en la [**propiedad Resumen del**](revision-number-summary.md) número de revisión del flujo de información de [resumen](summary-information-stream.md). Tenga en cuenta que las letras del código de producto y los GUID del código de paquete deben estar en mayúsculas. Utilidades como GUIDGEN generan GUID que contienen letras minúsculas. Las letras minúsculas de estos GUID deben cambiarse a mayúsculas para que se utilicen como código de producto o código de paquete.

Aunque es habitual enviar una aplicación que tiene el mismo código de paquete y código de producto, los dos valores pueden divergen a medida que se actualiza la aplicación. Por ejemplo, incluir un nuevo archivo con la aplicación requeriría actualizar la base de datos de instalación para instalar el archivo. Si los cambios son menores, un desarrollador puede optar por no cambiar el código del producto; sin embargo, se necesita otro archivo .msi para instalar el nuevo archivo, por lo que el código del paquete debe incrementarse. Por el contrario, se puede usar un único paquete para instalar más de un producto. Por ejemplo, la instalación de un paquete sin una transformación de idioma podría instalar la versión en inglés de la aplicación y la instalación del mismo paquete con una transformación de idioma podría instalar la versión en francés. La transformación es distinta del archivo .msi que determina el código del paquete. Las versiones en inglés y francés podrían tener códigos de producto diferentes y el mismo código de paquete porque ambos se instalan con el mismo archivo .msi paquete.

 

 



