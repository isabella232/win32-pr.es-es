---
description: El Windows puede realizar una instalación administrativa de una aplicación o un producto en una red para su uso por parte de un grupo de trabajo.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Instalación administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26968b6b81c1c2aafedfd74151b139f61062baa29c44b04977a119b14ab1a8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381855"
---
# <a name="administrative-installation"></a>Instalación administrativa

El Windows puede realizar una instalación administrativa de una aplicación o un producto en una red para su uso por parte de un grupo de trabajo. Una instalación administrativa instala una imagen de origen de la aplicación en la red que es similar a una imagen de origen en un CD-ROM. Los usuarios de un grupo de trabajo que tienen acceso a esta imagen administrativa pueden instalar el producto desde este origen. Un usuario debe instalar primero el producto desde la red para ejecutar la aplicación. El usuario puede elegir ejecutar desde el origen cuando se instala y el instalador usa la mayoría del archivo del producto directamente desde la red.

Los administradores pueden ejecutar una instalación administrativa desde la línea de comandos mediante la opción de línea [de comandos](command-line-options.md)/a .

La [acción ADMIN es](admin-action.md) la acción de nivel superior que se usa para iniciar una instalación administrativa. Cuando se ejecuta esta acción, el instalador llama a las acciones de las tablas [AdminExecuteSequence](adminexecutesequence-table.md) y [AdminUISequence](adminuisequence-table.md) para realizar la instalación administrativa.

La [**propiedad AdminProperties**](adminproperties.md) es una lista delimitada por punto y coma de propiedades que se establecen en el momento de una instalación de administración. El instalador usa estas propiedades durante una instalación posterior a la administración de la aplicación desde la imagen administrativa.

Los usuarios que no tienen acceso continuo a la red pueden instalar una aplicación desde una imagen administrativa y, a veces, tener que basarse en medios, como discos CD-ROM, como origen de copia de seguridad. En estos casos, la longitud de los nombres de archivo en la imagen administrativa y en el medio debe coincidir. Ambos deben usar nombres de archivo largos o ambos deben usar nombres de archivo cortos. Por ejemplo, un CD-ROM que solo admite nombres de archivo cortos podría proporcionar el medio original para instalar la imagen administrativa y un origen de copia de seguridad.

Si la [**propiedad SHORTFILENAMES**](shortfilenames.md) se establece durante una instalación administrativa, es posible que un usuario deba volver a establecer esta propiedad aplicando posteriormente una revisión a la imagen administrativa. Al usar Windows Installer para aplicar la revisión, el instalador establece automáticamente la propiedad **SHORTFILENAMES** si la imagen administrativa usa nombres de archivo cortos.

Si un administrador usa un paquete que tiene una propiedad [**Resumen**](word-count-summary.md) de recuento de palabras de 2 o 3 para realizar una instalación administrativa, los usuarios de la imagen administrativa no podrán reinstalar automáticamente desde el origen multimedia original. Si la imagen administrativa deja de estar disponible, se impide que los usuarios que se han instalado desde la imagen administrativa vuelvan al medio original.

La aplicación de [*transformaciones*](t-gly.md) durante la creación de una imagen administrativa no tiene ningún efecto válido. Para que una versión personalizada de un producto esté disponible para un grupo de trabajo, aplique la transformación durante la instalación del producto desde la imagen administrativa.

Durante una instalación administrativa, el instalador crea una imagen de origen para todas las características del producto, excepto las características con 0 en la columna Nivel de la [tabla Característica](feature-table.md).

 

 



