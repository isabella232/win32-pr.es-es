---
description: En este ejemplo se muestra cómo se puede utilizar una transformación de personalización para deshabilitar características y agregar nuevos recursos.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Ejemplo de transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652634"
---
# <a name="a-customization-transform-example"></a>Ejemplo de transformación de personalización

En este ejemplo se muestra cómo se puede utilizar una transformación de personalización para deshabilitar características y agregar nuevos recursos.

Un administrador puede deshabilitar una característica de forma permanente mediante una transformación de personalización para escribir un 0 en la columna de nivel de la [tabla de características](feature-table.md). A continuación, la aplicación de la transformación de personalización evita la instalación y visualización de esa característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo la propiedad [**AddLocal**](addlocal.md) en All en la línea de comandos. Para obtener una explicación del nivel de instalación, consulte la [tabla de características](feature-table.md) y la propiedad [**INSTALLLEVEL**](installlevel.md) .

Los recursos necesarios para personalizar una aplicación se pueden implementar mediante una transformación de personalización para agregar uno o más componentes nuevos. La transformación debe agregar una o varias características nuevas que contengan estos nuevos componentes. Para las reglas que deben seguirse al implementar recursos, como archivos, claves del registro o accesos directos, vea [usar transformaciones para agregar recursos](using-transforms-to-add-resources.md).

En este ejemplo se muestra cómo crear una [transformación](transforms.md) para personalizar la instalación de la aplicación descrita en [un ejemplo de instalación](an-installation-example.md). El paquete de instalación original instala todas las características de la aplicación de ejemplo, incluida la puerta de características, que permite a los usuarios ver la información de las admisiones del terreno de estacionamiento rojo. Algunos grupos de usuarios solo necesitan las características de aplicación que proporcionan información de programación de eventos y no necesitan la característica de puerta. Estos grupos también necesitan obtener una lista de teléfonos especiales. Por lo tanto, la transformación debe hacer dos cosas: 1) personalizar la instalación para que este grupo solo reciba las características de la aplicación que necesitan y 2) proporcionar los recursos necesarios para la nueva lista de teléfonos.

Un ejemplo de una interfaz de usuario mínima para este ejemplo se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) como Uisample.msi de archivos. Si tiene el SDK de, tendrá acceso a todas las herramientas y los datos necesarios para reproducir el paquete de instalación de ejemplo, la interfaz de usuario y la transformación de personalización.

La transformación de personalización tiene las siguientes especificaciones:

-   La transformación de personalización se incrusta dentro del archivo MNP2000.msi para garantizar que siempre está disponible con la base de datos de instalación.
-   La instalación de MNP2000.msi con la transformación de personalización no instala la característica de puerta, las características secundarias de la característica de la puerta ni ninguno de los componentes de la característica de la puerta, aunque el usuario seleccione el tipo completo de instalación.
-   Otras aplicaciones pueden compartir algunos o todos los componentes de la característica de la puerta. Los paquetes de instalación de estas aplicaciones pueden instalar todos sus componentes en el equipo del usuario.
-   Al quitar MNP2000.msi con la transformación de personalización no se quita ninguno de los componentes de la puerta instalados por otras aplicaciones.
-   La instalación de MNP2000.msi con la transformación de personalización también instala una nueva característica de nivel superior, la lista de teléfonos \_ y un nuevo componente, el teléfono, que requiere la instalación del recurso, Phone.txt. El usuario accede a la \_ característica de lista de teléfonos mediante un acceso directo en el directorio de menús.

[Continuar](customizing-an-original-database.md)

 

 



