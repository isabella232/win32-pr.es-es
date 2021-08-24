---
description: La acción RemoveExistingProducts pasa por los códigos de producto enumerados en la columna ActionProperty de la tabla Upgrade y quita los productos en secuencia invocando instalaciones simultáneas.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Acción RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3118ebd01aa39b0d9a5dad29ad1c3563c869ed5e0ebc8dfefd5ecd5c89301f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810935"
---
# <a name="removeexistingproducts-action"></a>Acción RemoveExistingProducts

La acción RemoveExistingProducts pasa por los códigos de producto enumerados en la columna ActionProperty de la tabla [Upgrade](upgrade-table.md) y quita los productos en secuencia invocando instalaciones simultáneas. Para cada instalación simultánea, el instalador establece la propiedad [**ProductCode**](productcode.md) en el código de producto y establece la propiedad [**REMOVE**](remove.md) en el valor del campo Quitar de la tabla Upgrade. Si el campo Quitar está en blanco, su valor predeterminado es ALL y el instalador quita todo el producto.

El instalador solo ejecuta la acción RemoveExistingProducts la primera vez que instala un producto. No ejecuta la acción durante una instalación [o](maintenance-installation.md) desinstalación de mantenimiento.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveExistingProducts debe programarse en la secuencia de acciones en una de las siguientes ubicaciones.

-   Entre la [acción InstallValidate](installvalidate-action.md) y [la acción InstallInitialize](installinitialize-action.md). En este caso, el instalador quita las aplicaciones antiguas por completo antes de instalar las nuevas aplicaciones. Se trata de una ubicación ineficaz para la acción porque todos los archivos reutilizados deben volver a copiarse.
-   Después de [la acción InstallInitialize y antes](installinitialize-action.md) de cualquier acción que genere el script de ejecución.
-   Entre la [acción InstallExecute](installexecute-action.md)o [installExecuteAgain](installexecuteagain-action.md)y [la acción InstallFinalize](installfinalize-action.md). Por lo general, las tres últimas acciones se programan una tras otra: InstallExecute, RemoveExistingProducts e InstallFinalize. En este caso, los archivos actualizados se instalan primero y, a continuación, se quitan los archivos antiguos. Sin embargo, si se produce un error en la eliminación de la aplicación antigua, el instalador revierte tanto la eliminación de la aplicación anterior como la instalación de la nueva aplicación.
-   Después de [la acción InstallFinalize](installfinalize-action.md). Esta es la ubicación más eficaz para la acción. En este caso, el instalador actualiza los archivos antes de quitar las aplicaciones antiguas. Solo los archivos que se actualizan se instalan durante la instalación. Si se produce un error en la eliminación de la aplicación anterior, el instalador solo revierte la desinstalación de la aplicación antigua.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Se ha quitado el producto.           |



 

## <a name="remarks"></a>Comentarios

Windows El instalador establece la [**propiedad UPGRADINGPRODUCTCODE**](upgradingproductcode.md) cuando ejecuta esta acción.

 

 



