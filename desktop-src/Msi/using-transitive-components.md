---
description: Un uso típico de los componentes transitivos es preparar un producto para reinstalar durante una actualización del sistema.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Uso de componentes transitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003474"
---
# <a name="using-transitive-components"></a>Uso de componentes transitivos

Un uso típico de los componentes transitivos es preparar un producto para reinstalar durante una actualización del sistema. El autor del paquete de instalación especifica los componentes que se deben intercambiar durante una actualización del sistema como si tuviera el atributo transitivo. Cuando el usuario actualiza el sistema posteriormente, se debe volver a instalar el producto. Tras la reinstalación, el instalador quita los componentes anteriores e instala los componentes posteriores, sin tener que instalar todo el producto.

**Para incluir dos componentes transitivos en el paquete de instalación**

1.  Incluya ambos componentes transitivos en el paquete de instalación.
2.  Cree ambos componentes transitivos en la [tabla de componentes](component-table.md) igual que los componentes normales. Cada componente transitivo debe tener su propio GUID único especificado en la columna ComponentId.
3.  Incluya el bit **msidbComponentAttributesTransitive** en la columna Attributes de la tabla de componentes para cada componente transitivo. Si se establece este bit, el instalador vuelve a evaluar el valor de la instrucción en la columna condición tras una reinstalación.

    Si el valor era previamente false y ha cambiado a true, el instalador instala el componente.

    Si el valor era previamente true y ha cambiado a false, el instalador quita el componente aunque el componente tenga otros productos como clientes.

    > [!Note]  
    > A menos que se establezca el bit transitivo, el componente permanece habilitado una vez instalado aunque la instrucción condicional se evalúe como false en una instalación posterior del mantenimiento del producto. Las condiciones deben basarse únicamente en los Estados de los equipos. No use con condiciones basadas en los Estados de usuario o las propiedades establecidas en la línea de comandos, ya que esto puede hacer que el instalador requiera una reinstalación del producto en cada uso por parte de un usuario diferente.

     

4.  Escriba expresiones condicionales complementarias en los campos condición de la tabla de control, de modo que cuando la condición del primer componente transitiva cambie a false, la condición del segundo componente transitivo cambie a true. Esto da como resultado la eliminación del primer componente y la instalación del segundo componente después de la reinstalación de la aplicación.

Es necesario volver a instalar el producto para cambiar los componentes transitivos. Por lo tanto, los autores de paquetes deben proporcionar a los usuarios un método para reinstalar el producto y establecer los modos de la propiedad [**REINSTALLMODE**](reinstallmode.md) . Básicamente, hay tres maneras de desencadenar la reinstalación:

-   Ejecute y configure la reinstalación a través de la interfaz de usuario mediante la creación de un paquete que use la interfaz de usuario [*completa*](f-gly.md).
-   Ejecute la reinstalación desde la línea de comandos mediante **msiexec/f** y seleccione los modos en la lista para la opción de la [línea de comandos](command-line-options.md) **/f** .
-   Haga que la aplicación llame a [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) o [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

El bit solo debe usarse con condiciones basadas en Estados de equipos. No use con condiciones basadas en los Estados de usuario o las propiedades establecidas en la línea de comandos, ya que esto puede hacer que el instalador requiera una reinstalación del producto en cada uso por parte de un usuario diferente.

> [!Note]
> A menos que se establezca el bit transitivo en la columna Attributes para un componente, el componente permanece habilitado una vez instalado aunque la instrucción condicional de la columna condition se evalúe como false en una instalación de mantenimiento posterior del producto.
> 
> En la mayoría de los casos, si una aplicación incluye componentes transitivos, Windows Installer requiere que el origen de la aplicación repare o actualice la aplicación. En estos casos, el CD-ROM de restauración del sistema enviado por un fabricante de equipos originales no funciona y es necesario proporcionar un origen de instalación real para la aplicación.

 

 

 



