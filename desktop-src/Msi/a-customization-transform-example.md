---
description: En este ejemplo se muestra cómo se puede usar una transformación de personalización para deshabilitar características y agregar nuevos recursos.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Un ejemplo de transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159284"
---
# <a name="a-customization-transform-example"></a>Un ejemplo de transformación de personalización

En este ejemplo se muestra cómo se puede usar una transformación de personalización para deshabilitar características y agregar nuevos recursos.

Un administrador puede deshabilitar permanentemente una característica mediante una transformación de personalización para escribir un 0 en la columna Nivel de la [tabla Característica](feature-table.md). A continuación, la aplicación de la transformación de personalización impide la instalación y presentación de esa característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo la propiedad [**ADDLOCAL**](addlocal.md) en ALL en la línea de comandos. Para obtener una explicación del nivel de instalación, vea [Tabla de características](feature-table.md) y Propiedad [**INSTALLLEVEL.**](installlevel.md)

Los recursos necesarios para personalizar una aplicación se pueden implementar mediante una transformación de personalización para agregar uno o varios componentes nuevos. La transformación debe agregar una o varias características nuevas para contener estos nuevos componentes. Para ver las reglas que se deben seguir al implementar recursos, como archivos, claves del Registro o accesos directos, vea Usar transformaciones [para agregar recursos.](using-transforms-to-add-resources.md)

En este ejemplo se muestra cómo crear una [transformación para](transforms.md) personalizar la instalación de la aplicación descrita en Un ejemplo [de instalación](an-installation-example.md). El paquete de instalación original instala todas las características de la aplicación de ejemplo, incluida la característica Puerta, que permite a los usuarios ver la información de admisión de Red Park Arena. Algunos grupos de usuarios solo necesitan las características de la aplicación que ofrecen información de programación de eventos y no necesitan la característica Puerta. Estos grupos también necesitan obtener una lista de teléfonos especial. Por lo tanto, la transformación debe hacer dos cosas: 1) personalizar la instalación para que este grupo solo reciba las características de la aplicación que necesitan y 2) proporcionar los recursos necesarios para la nueva lista de teléfonos.

Se proporciona un ejemplo de una interfaz de usuario mínima para este ejemplo en Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) como el archivo Uisample.msi. Si tiene el SDK, tiene acceso a todas las herramientas y datos necesarios para reproducir el paquete de instalación de ejemplo, la interfaz de usuario y la transformación de personalización.

La transformación de personalización tiene las siguientes especificaciones:

-   La transformación de personalización se inserta dentro del MNP2000.msi para garantizar que siempre está disponible con la base de datos de instalación.
-   Al instalar MNP2000.msi con la transformación de personalización no se instala la característica Puerta, las características secundarias de la característica Puerta ni ninguno de los componentes de la característica Puerta, incluso si el usuario selecciona el tipo completo de instalación.
-   Otras aplicaciones pueden compartir algunos o todos los componentes de la característica Puerta. Los paquetes de instalación de estas aplicaciones pueden instalar todos sus componentes en el equipo del usuario.
-   Al quitar MNP2000.msi con la transformación de personalización no se quita ninguno de los componentes de puerta instalados por otras aplicaciones.
-   La MNP2000.msi con la transformación de personalización también instala una nueva característica de nivel superior, Teléfono List, y un nuevo componente, phone, que requiere la instalación del \_ recurso, Phone.txt. El usuario accede a la Teléfono \_ list mediante un acceso directo en el directorio Menu.

[Continuar](customizing-an-original-database.md)

 

 



