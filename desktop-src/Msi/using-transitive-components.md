---
description: Un uso típico de los componentes transitivos es preparar un producto para volver a instalarlo durante una actualización del sistema.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Uso de componentes transitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ad6906b3e5d29ba6c0e3f8e279f4a1df2d5578f931219b6962062efaabd375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622893"
---
# <a name="using-transitive-components"></a>Uso de componentes transitivos

Un uso típico de los componentes transitivos es preparar un producto para volver a instalarlo durante una actualización del sistema. El autor del paquete de instalación especifica los componentes que deben intercambiarse durante una actualización del sistema como que tienen el atributo transitivo. Cuando el usuario actualice posteriormente el sistema, el producto debe volver a instalarse. Tras esta reinstalación, el instalador quita los componentes anteriores e instala los componentes posteriores, sin tener que instalar todo el producto.

**Para incluir dos componentes transitivos en el paquete de instalación**

1.  Incluya ambos componentes transitivos en el paquete de instalación.
2.  Cree ambos componentes transitivos en la [tabla Componente](component-table.md) igual que los componentes normales. Cada componente transitivo debe tener su propio GUID único especificado en la columna ComponentId.
3.  Incluya el **bit msidbComponentAttributesTransitive** en la columna Atributos de la tabla Component para cada componente transitivo. Si se establece este bit, el instalador vuelve a evaluar el valor de la instrucción en la columna Condición tras una reinstalación.

    Si el valor era false anteriormente y ha cambiado a True, el instalador instala el componente.

    Si el valor era true anteriormente y ha cambiado a False, el instalador quita el componente incluso si el componente tiene otros productos como clientes.

    > [!Note]  
    > A menos que se establezca el bit transitivo, el componente permanece habilitado una vez instalado, incluso si la instrucción condicional se evalúa como False en una instalación de mantenimiento posterior del producto. Las condiciones solo deben basarse en los estados del equipo. No use con condiciones basadas en estados de usuario o propiedades establecidas en la línea de comandos, ya que esto puede hacer que el instalador requiera una reinstalación del producto en cada uso por parte de un usuario diferente.

     

4.  Escriba expresiones condicionales complementarias en los campos Condición de la tabla Control de modo que cuando la condición del primer componente transitivo cambie a False, la condición del segundo componente transitivo cambie a True. Esto da como resultado la eliminación del primer componente y la instalación del segundo componente tras la reinstalación de la aplicación.

Es necesario volver a instalar el producto para cambiar los componentes transitivos. Por lo tanto, los autores de paquetes deben proporcionar a los usuarios un método para volver a instalar el producto y para establecer los modos de la [**propiedad REINSTALLMODE.**](reinstallmode.md) Básicamente hay tres maneras de desencadenar la reinstalación:

-   Ejecute y configure la reinstalación a través de la interfaz de usuario mediante la creación de un paquete que use la [*interfaz de usuario completa.*](f-gly.md)
-   Ejecute la reinstalación desde la línea de comandos mediante **msiexec /f** y seleccione los modos de la lista para la opción de línea [de comandos](command-line-options.md) **/f** .
-   Llame a la [**aplicación MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) [**o MsiReInstallFeature.**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)

El bit solo debe usarse con condiciones basadas en los estados del equipo. No use con condiciones basadas en estados de usuario o propiedades establecidas en la línea de comandos, ya que esto puede hacer que el instalador requiera una reinstalación del producto en cada uso por parte de un usuario diferente.

> [!Note]
> A menos que el bit transitivo de la columna Atributos esté establecido para un componente, el componente permanece habilitado una vez instalado incluso si la instrucción condicional de la columna Condición se evalúa como False en una instalación de mantenimiento posterior del producto.
> 
> En la mayoría de los casos, si una aplicación incluye componentes transitivos, Windows Installer requiere que el origen de la aplicación repare o actualice la aplicación. En estos casos, el CD-ROM de restauración del sistema enviado por un fabricante de equipos originales no funciona y es necesario proporcionar un origen de instalación real para la aplicación.

 

 

 



