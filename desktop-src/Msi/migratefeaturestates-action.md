---
description: La acción MigrateFeatureStates se usa durante la actualización y al instalar una nueva aplicación en una aplicación relacionada.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Acción MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678214"
---
# <a name="migratefeaturestates-action"></a>Acción MigrateFeatureStates

La acción MigrateFeatureStates se usa durante la actualización y al instalar una nueva aplicación en una aplicación relacionada. MigrateFeatureStates Lee los Estados de las características en la aplicación existente y, a continuación, establece estos Estados de características en la instalación pendiente. El método solo es útil cuando el nuevo árbol de características no ha cambiado en gran medida del original.

La acción MigrateFeatureStates solo se ejecuta la primera vez que se instala el producto. La acción MigrateFeatureStates no se ejecuta durante el modo de mantenimiento o la desinstalación.

La acción MigrateFeatureStates se ejecuta a través de cada registro de la [tabla de actualización](upgrade-table.md) en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con todos los productos instalados en el sistema. Si la acción MigrateFeatureStates detecta una correspondencia y se establece la marca de bits msidbUpgradeAttributesMigrateFeatures en la columna Attributes de la tabla upgrade, el instalador consulta los Estados de característica existentes para el producto y establece estos Estados para las mismas características en la nueva aplicación. La acción solo migra los Estados de la característica si no se establece la propiedad [**preseleccionada**](preselected.md) .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MigrateFeatureStates debe aparecer inmediatamente después de la [acción CostFinalize](costfinalize-action.md). MigrateFeatureStates se debe secuenciar tanto en la [tabla InstallUISequence](installuisequence-table.md) como en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que MigrateFeatureStates se ejecute en InstallExecuteSequence si la acción ya se ejecutó en InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData

MigrateFeatureSettings envía un mensaje de datos de acción para cada producto.

## <a name="remarks"></a>Observaciones

Si más de un producto instalado comparte una característica, el estado de la instalación de esa característica puede diferir entre los productos. La acción MigrateFeatureState usa el orden de prioridad siguiente al migrar los Estados de instalación de características: ejecutar local, ejecutar desde el origen, anunciado y desinstalar. Por ejemplo, el producto A instalado puede tener la característica Y como INSTALLSTATE \_ local y el producto instalado B puede tener la característica y como installstate \_ ausente. Si una actualización instala el producto C y migra el estado de instalación de la característica Y, MigrateFeatureState establece el estado de instalación de la característica Y en el producto C en INSTALLSTATE \_ local.

Para obtener más información sobre cómo usar la acción MigrateFeatureStates para las actualizaciones de productos, consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).

 

 



