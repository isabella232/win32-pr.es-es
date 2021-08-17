---
description: La acción RemoveRegistryValues solo puede quitar valores del Registro del sistema que se hayan escrito en la tabla Registry o en la tabla RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Acción RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fe284043f76cbffe3fe6a6887f46d6ab16ba65e9103efce6e4e62baac31d31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339665"
---
# <a name="removeregistryvalues-action"></a>Acción RemoveRegistryValues

La acción RemoveRegistryValues solo puede quitar valores del Registro del sistema que se hayan escrito en la tabla [Registry](registry-table.md) o en la [tabla RemoveRegistry](removeregistry-table.md). Esta acción quita un valor del Registro que se ha escrito en la tabla del Registro si el componente asociado se instaló localmente o como ejecutado desde el origen y ahora está configurado para desinstalarse. Esta acción quita un valor del Registro que se ha escrito en la tabla RemoveRegistry si el componente asociado está establecido para instalarse localmente o como ejecutado desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveRegistryValues. Si se [usa una acción WriteRegistryValues,](writeregistryvalues-action.md) debe ir después de RemoveRegistryValues. RemoveRegistryValues debe ir antes [de UnregisterMIMEInfo](unregistermimeinfo-action.md) o [UnregisterProgIDInfo.](unregisterprogidinfo-action.md)

Se puede usar una acción personalizada para agregar filas a la tabla [del Registro](registry-table.md) durante una transacción de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del Registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada debe ejecutarse en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ir antes de las acciones RemoveRegistryValues y [WriteRegistryValues](writeregistryvalues-action.md) en la secuencia de acciones.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                          |
|-------|-----------------------------------------------------|
| \[1\] | Ruta de acceso del Registro a la clave del valor del Registro quitado.     |
| \[2\] | Cadena con formato del nombre del valor del Registro quitado. |



 

## <a name="remarks"></a>Comentarios

Para quitar un valor del Registro, registre el valor en la columna Valor de la tabla Registro. Si la acción WriteRegistryValues ha adjuntado cadenas REG MULTI SZ al valor de la tabla Registry , la acción \_ \_ RemoveRegistryValues [](registry-table.md)quita solo esas cadenas del valor del Registro.

 

 



