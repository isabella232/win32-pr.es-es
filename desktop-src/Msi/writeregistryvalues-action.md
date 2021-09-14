---
description: La acción WriteRegistryValues configura la información del Registro de una aplicación.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: WriteRegistryValues (Acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071800"
---
# <a name="writeregistryvalues-action"></a>WriteRegistryValues (Acción)

La acción WriteRegistryValues configura la información del Registro de una aplicación. La información del Registro se puede obtener mediante la [tabla Component](component-table.md). Se escribe un valor del Registro en el registro si el componente correspondiente se ha establecido para instalarse localmente o como ejecutado desde el origen. Para obtener más información, vea [Tabla del Registro](registry-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate debe](installvalidate-action.md) ir antes de la acción WriteRegistryValues. Si hay una [acción RemoveRegistryValues](removeregistryvalues-action.md), debe ir antes de la acción WriteRegistryValues.

Se puede usar una acción personalizada para agregar filas a la tabla [del Registro](registry-table.md) durante una transacción de instalación, desinstalación o reparación. Estas filas no se conservan en la tabla del Registro y la información solo está disponible durante la transacción actual. Por lo tanto, la acción personalizada debe ejecutarse en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales. La acción personalizada debe ir antes de [las acciones RemoveRegistryValues](removeregistryvalues-action.md) y WriteRegistryValues en la secuencia de acciones.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                               |
|-------|----------------------------------------------------------|
| \[1\] | Ruta de acceso a la clave del Registro del valor escrito en el Registro.       |
| \[2\] | Nombre de cadena de texto con formato del valor escrito en el Registro. |
| \[3\] | Cadena de texto con formato de valor escrita en el Registro.      |



 

 

 



