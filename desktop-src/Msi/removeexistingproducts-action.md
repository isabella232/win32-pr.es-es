---
description: La acción RemoveExistingProducts recorre los códigos de producto que se muestran en la columna ActionProperty de la tabla de actualización y quita los productos en secuencia mediante la invocación de instalaciones simultáneas.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Acción RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667470"
---
# <a name="removeexistingproducts-action"></a>Acción RemoveExistingProducts

La acción RemoveExistingProducts recorre los códigos de producto que se muestran en la columna ActionProperty de la [tabla de actualización](upgrade-table.md) y quita los productos en secuencia mediante la invocación de instalaciones simultáneas. Para cada instalación simultánea, el instalador establece la propiedad [**ProductCode**](productcode.md) en el código de producto y establece la propiedad [**Remove**](remove.md) en el valor del campo Remove de la tabla de actualización. Si el campo quitar está en blanco, su valor predeterminado es todos y el instalador quita todo el producto.

El instalador solo ejecuta la acción RemoveExistingProducts la primera vez que instala un producto. No ejecuta la acción durante una instalación o desinstalación de [mantenimiento](maintenance-installation.md) .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveExistingProducts se debe programar en la secuencia de acciones en una de las siguientes ubicaciones.

-   Entre la [acción InstallValidate](installvalidate-action.md) y la [acción InstallInitialize](installinitialize-action.md). En este caso, el instalador quita las aplicaciones antiguas completamente antes de instalar las nuevas aplicaciones. Se trata de una ubicación ineficaz para la acción, ya que todos los archivos reutilizados deben volver a copiarse.
-   Después de la [acción InstallInitialize](installinitialize-action.md) y antes de cualquier acción que genere el script de ejecución.
-   Entre la [acción InstallExecute](installexecute-action.md), la [acción InstallExecuteAgain](installexecuteagain-action.md)y la [acción InstallFinalize](installfinalize-action.md). Por lo general, las tres últimas acciones se programan justo después de otra: InstallExecute, RemoveExistingProducts y InstallFinalize. En este caso, los archivos actualizados se instalan primero y, a continuación, se quitan los archivos antiguos. Sin embargo, si se produce un error en la eliminación de la aplicación anterior, el instalador revierte tanto la eliminación de la aplicación anterior como la instalación de la nueva aplicación.
-   Después de la [acción InstallFinalize](installfinalize-action.md). Esta es la ubicación más eficaz para la acción. En este caso, el instalador actualiza los archivos antes de quitar las aplicaciones antiguas. Solo los archivos que se van a actualizar se instalan durante la instalación. Si se produce un error en la eliminación de la aplicación anterior, el instalador solo revierte la desinstalación de la aplicación anterior.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Se quitó el producto.           |



 

## <a name="remarks"></a>Observaciones

Windows Installer establece la propiedad [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) cuando se ejecuta esta acción.

 

 



