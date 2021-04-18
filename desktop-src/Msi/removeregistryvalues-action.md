---
description: La acción RemoveRegistryValues solo puede quitar valores del registro del sistema que se han creado en la tabla del registro o en la tabla RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Acción RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667670"
---
# <a name="removeregistryvalues-action"></a>Acción RemoveRegistryValues

La acción RemoveRegistryValues solo puede quitar valores del registro del sistema que se han creado en la [tabla del registro](registry-table.md) o en la [tabla RemoveRegistry](removeregistry-table.md). Esta acción quita un valor del registro que se ha creado en la tabla del registro si el componente asociado se instaló localmente o como ejecutado desde el origen y ahora está configurado para desinstalarse. Esta acción quita un valor del registro que se ha creado en la tabla RemoveRegistry si el componente asociado está configurado para instalarse localmente o como ejecutar desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveRegistryValues. Si se usa una acción [WriteRegistryValues](writeregistryvalues-action.md) , debe aparecer después de RemoveRegistryValues. RemoveRegistryValues debe ser anterior a [UnregisterMIMEInfo](unregistermimeinfo-action.md) o [UnregisterProgIDInfo](unregisterprogidinfo-action.md).

Se puede utilizar una acción personalizada para agregar filas a la [tabla del registro](registry-table.md) durante una operación de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ser anterior a las acciones RemoveRegistryValues y [WriteRegistryValues](writeregistryvalues-action.md) en la secuencia de acción.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                          |
|-------|-----------------------------------------------------|
| \[1\] | Ruta de acceso del registro a la clave del valor del registro que se ha quitado.     |
| \[2\] | Cadena con formato del nombre del valor del registro que se ha quitado. |



 

## <a name="remarks"></a>Observaciones

Para quitar un valor del registro, grabe el valor en la columna valor de la tabla del registro. Si la acción de WriteRegistryValues ha adjuntado las cadenas de REG \_ multi \_ SZ al valor de la [tabla del registro](registry-table.md), la acción RemoveRegistryValues quita solo esas cadenas del valor del registro.

 

 



