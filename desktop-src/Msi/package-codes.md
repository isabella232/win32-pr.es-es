---
description: El código del paquete es un GUID que identifica un paquete de Windows Installer determinado.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Códigos de paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156317"
---
# <a name="package-codes"></a>Códigos de paquete

El código del paquete es un GUID que identifica un [*paquete*](p-gly.md)de Windows Installer determinado. El código del paquete asocia un archivo. msi a una aplicación o un producto y también se puede usar para la comprobación de orígenes. Los códigos de producto y paquete no son intercambiables. Para obtener más información, consulte [códigos de producto](product-codes.md).

Los archivos. msi no idénticos no deben tener el mismo código de paquete. Es importante cambiar el código de paquete porque es el identificador principal que usa el instalador para buscar y validar el paquete correcto para una instalación determinada. Si se cambia un paquete sin cambiar el código de paquete, es posible que el instalador no use el paquete más reciente si ambos siguen siendo accesibles para el instalador.

El código del paquete se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) de la secuencia de información de [Resumen](summary-information-stream.md). Tenga en cuenta que las letras del código de producto y los GUID de código de paquete deben estar en mayúsculas. Las utilidades como GUIDGEN generan GUID que contienen letras minúsculas. Las letras minúsculas de estos GUID deben cambiarse a mayúsculas para usarse como código de producto o código de paquete.

Aunque es habitual enviar una aplicación que tenga el mismo código de paquete y el mismo código de producto, los dos valores pueden diferir a medida que se actualiza la aplicación. Por ejemplo, si se incluye un archivo nuevo con la aplicación, es necesario actualizar la base de datos de instalación para instalar el archivo. Sin embargo, si los cambios son menores, es posible que un desarrollador decida no cambiar el código de producto, pero se necesita un archivo. msi diferente para instalar el nuevo archivo y, por tanto, se debe incrementar el código del paquete. A la inversa, se puede usar un único paquete para instalar más de un producto. Por ejemplo, la instalación de un paquete sin una transformación de idioma podría instalar la versión en Inglés de la aplicación y la instalación del mismo paquete con una transformación de idioma podría instalar la versión en francés. La transformación es distinta del archivo. msi que determina el código del paquete. Las versiones en inglés y en francés podrían tener distintos códigos de producto y el mismo código de paquete porque ambos se instalan con el mismo archivo. msi.

 

 



