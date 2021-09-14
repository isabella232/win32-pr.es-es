---
description: Las instalaciones simultáneas, también denominadas instalaciones anidadas, son una característica en desuso del Windows instalador.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Instalaciones simultáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158821"
---
# <a name="concurrent-installations"></a>Instalaciones simultáneas

Las instalaciones simultáneas, también denominadas instalaciones anidadas, son una característica en desuso del Windows instalador. Las aplicaciones instaladas con instalaciones simultáneas pueden producir un error porque son difíciles de dar servicio correctamente a los clientes. No use instalaciones simultáneas para instalar productos que estén diseñados para publicarse al público. Las instalaciones simultáneas pueden tener una aplicabilidad limitada en entornos corporativos controlados cuando se usan para instalar aplicaciones que no están diseñadas para la versión pública. La documentación de instalaciones simultáneas se proporciona para los autores de paquetes que desean usar instalaciones simultáneas con aplicaciones que no están para la distribución pública.

Una acción de instalación simultánea instala otro paquete Windows Installer durante una instalación que se está ejecutando actualmente. Una instalación simultánea se agrega a un paquete mediante la creación de una acción de instalación simultánea en la [tabla CustomAction](customaction-table.md) y la programación de esta acción personalizada en las tablas de secuencia. El campo Destino de la tabla CustomAction contiene una cadena de valores de propiedad pública utilizados por la instalación simultánea. El campo Source de la tabla CustomAction identifica el paquete simultáneo. Una acción de instalación simultánea solo puede reinstalar o quitar una aplicación instalada por el paquete de instalación de la aplicación actual.

El tipo de acción de instalación simultánea se especifica en el campo Tipo de la tabla CustomAction. Según el tipo de acción personalizada, el paquete de la aplicación simultánea puede residir en un subalmacenamiento del paquete principal, como un archivo en una ubicación especificada por una propiedad o como una aplicación anunciada en el equipo del usuario. Los siguientes tipos de acciones personalizadas realizan una instalación simultánea.



| Tipo de acción personalizada                                 | Descripción                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo de acción personalizada 7](custom-action-type-7.md)   | Instalación simultánea de un producto que reside en el paquete de instalación.      |
| [Tipo de acción personalizada 23](custom-action-type-23.md) | Instalación simultánea de un paquete de instalador en el árbol de origen actual. |
| [Tipo de acción personalizada 39](custom-action-type-39.md) | Instalación simultánea de un paquete de instalador anunciado.                     |



 

Una instalación simultánea comparte la misma interfaz de usuario y la misma configuración de registro que la instalación principal.

Las acciones de instalación simultáneas deben colocarse entre [la acción InstallInitialize](installinitialize-action.md) y [la acción InstallFinalize](installfinalize-action.md) de la secuencia de acciones de la instalación principal. Tras la reversión de la instalación principal, el instalador revertirá también la instalación simultánea. El uso [de la ejecución diferida](deferred-execution-custom-actions.md) con acciones de instalación simultáneas no es necesario porque el instalador combina la información de reversión de las instalaciones simultáneas y principales. Todos los cambios se invierten tras una instalación de reversión.

Los valores devueltos para las acciones de instalación simultáneas son los mismos que para otras acciones personalizadas. Vea [Valores devueltos de acciones personalizadas.](custom-action-return-values.md)

Las acciones estándar o personalizadas que especifican un reinicio automático del sistema, o solicitan al usuario que se reinicie, también pueden realizar el reinicio o la solicitud desde dentro de una instalación simultánea.

Una vez que el instalador comienza una instalación simultánea, bloquea todas las demás instalaciones hasta que se completa la instalación simultánea y antes de continuar con la instalación principal. El instalador solo puede ejecutar instalaciones simultáneas como acciones personalizadas sincrónicas. Vea [Acciones personalizadas sincrónicas y asincrónicas.](synchronous-and-asynchronous-custom-actions.md) Las marcas de opción descritas en [Custom Action Return Processing Options](custom-action-return-processing-options.md) deben establecerse en none (+0) o **msidbCustomActionTypeContinue** (+64).

Una acción de instalación simultánea puede instalar una aplicación para ejecutarse localmente, ejecutarse desde el origen, volver a instalarse o quitarse de la misma manera que cuando se usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para una instalación normal. Para especificar el tipo de instalación, pase la propiedad [**ADDLOCAL**](addlocal.md), [**ADDSOURCE**](addsource.md), [**REINSTALL**](reinstall.md)o [**REMOVE**](remove.md) a la acción de instalación simultánea.

Las acciones de instalación simultáneas se pueden crear en pares, una acción usada para la instalación y la otra acción usada para quitar la instalación simultánea. Normalmente [se usa un tipo de acción personalizada 7](custom-action-type-7.md) o un tipo de acción personalizada [23](custom-action-type-23.md) para instalar. Un [tipo de acción personalizada 39](custom-action-type-39.md) se usa normalmente para quitar la instalación simultánea cuando se desinstala el producto primario. El registro de la acción personalizada de eliminación en la [tabla CustomAction](customaction-table.md) puede tener el GUID del código de producto en el campo Origen y "REMOVE=ALL" en el campo Destino. Las dos acciones personalizadas deben crearse en la tabla de secuencia de acciones con condiciones mutuamente excluyentes. Por ejemplo, la acción personalizada que instala el producto puede tener "NOT Installed" en su campo Condición y la acción personalizada quita la instalación simultánea puede tener REMOVE="ALL" en su campo Condición.

No hay ningún método para consultar un paquete por su costo. Esto dificulta el costo de una instalación simultánea. Se deben agregar filas a la [tabla ReserveCost](reservecost-table.md) para indicar las carpetas y los costos en el peor de los casos del componente asociado a la instalación simultánea.

Las [únicas opciones de procesamiento](custom-action-return-processing-options.md) devuelto de acciones personalizadas disponibles con acciones de instalación simultáneas son none (+0) o **msidbCustomActionTypeContinue** (+64).

Tenga en cuenta que una instalación primaria no puede llamar a su propio paquete como una acción de instalación simultánea.

Tenga en cuenta que si una instalación por equipo intenta ejecutar una instalación simultánea por usuario, el instalador registra la instalación primaria como por usuario de forma predeterminada. Esto puede hacer que el instalador quite incorrectamente la aplicación porque el instalador intenta desinstalar la aplicación por equipo cuando realmente se registra como por usuario. Para forzar que el estado de una instalación simultánea realice un seguimiento del estado de su instalación primaria, escriba ALLUSERS=" ALLUSERS " en la columna Destino de la \[ \] tabla [CustomAction](customaction-table.md). En este caso, la instalación simultánea es por equipo si el elemento primario es por equipo y la instalación simultánea es por usuario si el elemento primario es por usuario.

Los desarrolladores deben tener en cuenta las siguientes advertencias al crear instalaciones simultáneas.

-   Las instalaciones simultáneas no pueden compartir componentes.
-   Una instalación administrativa tampoco puede contener una instalación simultánea.
-   Es posible que la aplicación de revisiones y la actualización no funcionen con instalaciones simultáneas.
-   Es posible que el instalador no coste correctamente una instalación simultánea.
-   Las ProgressBars integradas no se pueden usar con instalaciones simultáneas.
-   La instalación simultánea no puede instalar los recursos que se van a anunciar.
-   Un paquete que realiza una instalación simultánea de una aplicación también debe desinstalar la aplicación simultánea cuando se desinstala el producto primario.

Para evitar que un paquete se instale como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la [tabla LaunchCondition.](launchcondition-table.md) Esto evita que el paquete se instale alguna vez mediante una acción de instalación simultánea ejecutada por otra instalación. Esto no impide que la acción [RemoveExistingProducts](removeexistingproducts-action.md) quite el paquete. Vea también la [**propiedad ParentOriginalDatabase**](parentoriginaldatabase.md) y [**la propiedad ParentProductCode.**](parentproductcode.md)

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



