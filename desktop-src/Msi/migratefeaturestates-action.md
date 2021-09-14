---
description: La acción MigrateFeatureStates se usa durante la actualización y al instalar una nueva aplicación en una aplicación relacionada.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Acción MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261268"
---
# <a name="migratefeaturestates-action"></a>Acción MigrateFeatureStates

La acción MigrateFeatureStates se usa durante la actualización y al instalar una nueva aplicación en una aplicación relacionada. MigrateFeatureStates lee los estados de características de la aplicación existente y, a continuación, establece estos estados de características en la instalación pendiente. El método solo es útil cuando el nuevo árbol de características no ha cambiado mucho con el original.

La acción MigrateFeatureStates solo se ejecuta la primera vez que se instala el producto. La acción MigrateFeatureStates no se ejecuta durante el modo de mantenimiento o la desinstalación.

La acción MigrateFeatureStates se ejecuta a través de cada registro de la tabla [Upgrade](upgrade-table.md) en secuencia y compara el código de actualización, la versión del producto y el idioma de cada fila con todos los productos instalados en el sistema. Si la acción MigrateFeatureStates detecta una correspondencia y la marca de bits msidbUpgradeAttributesMigrateFeatures se establece en la columna Atributos de la tabla Upgrade, el instalador consulta los estados de características existentes para el producto y establece estos estados para las mismas características de la nueva aplicación. La acción solo migra los estados de característica si no se establece la propiedad [**Preselected.**](preselected.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MigrateFeatureStates debe ir inmediatamente después de [la acción CostFinalize](costfinalize-action.md). MigrateFeatureStates debe secuenciarse tanto en la tabla [InstallUISequence](installuisequence-table.md) como en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que MigrateFeatureStates se ejecute en InstallExecuteSequence si la acción ya se ha ejecutado en InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData

MigrateFeatureSettings envía un mensaje de datos de acción para cada producto.

## <a name="remarks"></a>Observaciones

Si más de un producto instalado comparte una característica, el estado de instalación de esa característica puede diferir entre los productos. La acción MigrateFeatureState usa el siguiente orden de prioridad al migrar los estados de instalación de características: ejecutar localmente, ejecutar desde el origen, anunciar y desinstalar. Por ejemplo, el producto instalado A puede tener la característica Y como INSTALLSTATE LOCAL y el producto B instalado puede tener la característica \_ Y como INSTALLSTATE \_ ABSENT. Si una actualización instala el producto C y migra el estado de instalación de la característica Y, MigrateFeatureState establece el estado de instalación de la característica Y del producto C en INSTALLSTATE \_ LOCAL.

Para obtener más información sobre cómo usar la acción MigrateFeatureStates para las actualizaciones de productos, vea Preparar una aplicación para futuras [actualizaciones principales.](preparing-an-application-for-future-major-upgrades.md)

 

 



