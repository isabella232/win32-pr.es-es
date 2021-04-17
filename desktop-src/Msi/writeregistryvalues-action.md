---
description: La acción WriteRegistryValues configura la información del registro de una aplicación.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Acción WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678019"
---
# <a name="writeregistryvalues-action"></a>Acción WriteRegistryValues

La acción WriteRegistryValues configura la información del registro de una aplicación. La información del registro se valida mediante la [tabla de componentes](component-table.md). Un valor del registro se escribe en el registro si se ha establecido que el componente correspondiente se instale localmente o como ejecutado desde el origen. Para obtener más información, vea [tabla del registro](registry-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate](installvalidate-action.md) debe ser anterior a la acción WriteRegistryValues. Si hay una [acción RemoveRegistryValues](removeregistryvalues-action.md), debe ser anterior a la acción WriteRegistryValues.

Se puede utilizar una acción personalizada para agregar filas a la [tabla del registro](registry-table.md) durante una operación de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ser anterior a las acciones [RemoveRegistryValues](removeregistryvalues-action.md) y WriteRegistryValues en la secuencia de acción.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                               |
|-------|----------------------------------------------------------|
| \[1\] | Ruta de acceso a la clave del registro del valor escrito en el registro.       |
| \[2\] | Nombre de cadena de texto con formato del valor escrito en el registro. |
| \[3\] | Cadena de texto con formato del valor escrito en el registro.      |



 

 

 



