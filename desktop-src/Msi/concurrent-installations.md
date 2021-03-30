---
description: Las instalaciones simultáneas, también denominadas instalaciones anidadas, son una característica desusada de la Windows Installer.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Instalaciones simultáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910986"
---
# <a name="concurrent-installations"></a>Instalaciones simultáneas

Las instalaciones simultáneas, también denominadas instalaciones anidadas, son una característica desusada de la Windows Installer. Es posible que se produzca un error en las aplicaciones instaladas con instalaciones simultáneas porque son difíciles de atender correctamente a los clientes. No use instalaciones simultáneas para instalar productos que están diseñados para publicarse en el público. Las instalaciones simultáneas pueden tener una aplicabilidad limitada en entornos corporativos controlados cuando se usan para instalar aplicaciones que no están destinadas a la versión pública. La documentación de instalaciones simultáneas se proporciona para los autores de paquetes que desean usar instalaciones simultáneas con aplicaciones que no son para la distribución pública.

Una acción de instalación simultánea instala otro paquete de Windows Installer durante una instalación en ejecución. Una instalación simultánea se agrega a un paquete mediante la creación de una acción de instalación simultánea en la [tabla CustomAction](customaction-table.md) y la programación de esta acción personalizada en las tablas de secuencia. El campo de destino de la tabla CustomAction contiene una cadena de valores de propiedad pública utilizada por la instalación simultánea. El campo de origen de la tabla CustomAction identifica el paquete simultáneo. Una acción de instalación simultánea solo puede reinstalar o quitar una aplicación que haya instalado el paquete de instalación de la aplicación actual.

El tipo de acción de instalación simultánea se especifica en el campo tipo de la tabla CustomAction. Dependiendo del tipo de acción personalizada, el paquete de la aplicación simultánea puede residir en un subalmacenamiento del paquete principal, como un archivo en una ubicación especificada por una propiedad o como una aplicación anunciada en el equipo del usuario. Los siguientes tipos de acciones personalizadas realizan una instalación simultánea.



| Tipo de acción personalizada                                 | Descripción                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo de acción personalizada 7](custom-action-type-7.md)   | Instalación simultánea de un producto que reside en el paquete de instalación.      |
| [Tipo de acción personalizada 23](custom-action-type-23.md) | Instalación simultánea de un paquete del instalador en el árbol de origen actual. |
| [Tipo de acción personalizada 39](custom-action-type-39.md) | Instalación simultánea de un paquete de instalador anunciado.                     |



 

Una instalación simultánea comparte la misma interfaz de usuario y la misma configuración de registro que la instalación principal.

Las acciones de instalación simultáneas se deben colocar entre la [acción InstallInitialize](installinitialize-action.md) y la [acción InstallFinalize](installfinalize-action.md) de la secuencia de acciones de la instalación principal. Tras la reversión de la instalación principal, el instalador revierte también la instalación simultánea. El uso de la [ejecución aplazada](deferred-execution-custom-actions.md) con acciones de instalación simultáneas no es necesario porque el instalador combina la información de reversión de las instalaciones simultáneas y principales. Todos los cambios se invierten en una instalación de reversión.

Los valores devueltos para las acciones de instalación simultáneas son los mismos que para otras acciones personalizadas. Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).

Acciones estándar o personalizadas que especifican un reinicio automático del sistema o solicitan al usuario que se reinicie, también pueden realizar el reinicio o la solicitud desde una instalación simultánea.

Una vez que el instalador inicia una instalación simultánea, bloquea todas las demás instalaciones hasta que se completa la instalación simultánea y antes de continuar con la instalación principal. El instalador solo puede ejecutar instalaciones simultáneas como acciones personalizadas sincrónicas. Vea [acciones personalizadas sincrónicas y asincrónicas](synchronous-and-asynchronous-custom-actions.md). Las marcas de opciones descritas en [Opciones de procesamiento de devolución de acción personalizadas](custom-action-return-processing-options.md) se deben establecer en ninguno (+ 0) o **msidbCustomActionTypeContinue** (+ 64).

Una acción de instalación simultánea puede instalar una aplicación para que se ejecute de forma local, ejecutar desde el origen, volver a instalar o quitar de la misma manera que cuando se usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para una instalación normal. Para especificar el tipo de instalación, pase la propiedad [**AddLocal**](addlocal.md), [**ADDSOURCE**](addsource.md), [**REINSTALL**](reinstall.md)o [**Remove**](remove.md) a la acción de instalación simultánea.

Las acciones de instalación simultáneas se pueden crear en pares, una acción que se usa para instalar y la otra acción que se usa para quitar la instalación simultánea. Normalmente, se usa una [acción personalizada tipo 7](custom-action-type-7.md) o [acción personalizada tipo 23](custom-action-type-23.md) para instalar. Un [tipo de acción personalizada 39](custom-action-type-39.md) se usa normalmente para quitar la instalación simultánea cuando se desinstala el producto primario. El registro de la acción personalizada de eliminación en la [tabla CustomAction](customaction-table.md) puede tener el GUID del código de producto en el campo de origen y "quitar = todos" en el campo de destino. Las dos acciones personalizadas deben crearse en la tabla de secuencia de acción con condiciones mutuamente excluyentes. Por ejemplo, la acción personalizada que instala el producto puede tener "no instalado" en su campo condición y la acción personalizada quita la instalación simultánea puede tener el campo quitar = "todo" en su condición.

No hay ningún método para consultar el costo de un paquete. Esto hace que el costo de una instalación simultánea sea difícil. Se deben agregar filas a la [tabla ReserveCost](reservecost-table.md) para indicar las carpetas y los costos peores del componente asociados a la instalación simultánea.

Las únicas [Opciones de procesamiento que devuelven la acción personalizada](custom-action-return-processing-options.md) disponibles con las acciones de instalación simultáneas son ninguno (+ 0) o **msidbCustomActionTypeContinue** (+ 64).

Tenga en cuenta que una instalación primaria no puede llamar a su propio paquete como una acción de instalación simultánea.

Tenga en cuenta que si una instalación por equipo intenta ejecutar una instalación simultánea por usuario, el instalador registra la instalación primaria como por usuario de forma predeterminada. Esto puede hacer que el instalador Quite incorrectamente la aplicación porque el instalador intenta desinstalar la aplicación por equipo cuando realmente se registra como por usuario. Para forzar el estado de una instalación simultánea a fin de realizar un seguimiento del estado de su instalación primaria, escriba ALLUSERS = " \[ AllUsers \] " en la columna target de la [tabla CustomAction](customaction-table.md). En este caso, la instalación simultánea es por equipo si el elemento primario es por equipo y la instalación simultánea es por usuario si el elemento primario es por usuario.

Los desarrolladores deben tener en cuenta las siguientes advertencias al crear instalaciones simultáneas.

-   Las instalaciones simultáneas no pueden compartir componentes.
-   Una instalación administrativa no puede contener también una instalación simultánea.
-   Es posible que la revisión y la actualización no funcionen con instalaciones simultáneas.
-   Es posible que el instalador no cueste correctamente una instalación simultánea.
-   Los ProgressBar integrados no se pueden usar con instalaciones simultáneas.
-   Los recursos que se van a anunciar no se pueden instalar mediante la instalación simultánea.
-   Un paquete que realiza una instalación simultánea de una aplicación también debe desinstalar la aplicación simultánea cuando se desinstale el producto primario.

Para evitar que un paquete se instale una vez como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la tabla [LaunchCondition](launchcondition-table.md) . Esto evita que el paquete se instale una acción de instalación simultánea ejecutada por otra instalación. Esto no impide que la acción [RemoveExistingProducts](removeexistingproducts-action.md) Quite el paquete. Vea también la propiedad [**ParentOriginalDatabase**](parentoriginaldatabase.md) y la propiedad [**ParentProductCode**](parentproductcode.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



