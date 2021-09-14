---
description: La acción WriteEnvironmentStrings modifica los valores de las variables de entorno.
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: WriteEnvironmentStrings (Acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071804"
---
# <a name="writeenvironmentstrings-action"></a>WriteEnvironmentStrings (Acción)

La acción WriteEnvironmentStrings modifica los valores de las variables de entorno.

Las variables de entorno no cambian para la instalación en curso cuando se ejecutan la acción WriteEnvironmentStrings o [RemoveEnvironmentStrings.](removeenvironmentstrings-action.md) En Windows 2000, Windows Server 2003, Windows XP y Windows Vista, esta información se almacena en el Registro y se envía un mensaje [**\_ WM SETTINGCHANGE**](../winmsg/wm-settingchange.md) para notificar al sistema los cambios cuando se complete la instalación. Otro proceso puede recibir una notificación de los cambios controlando estos mensajes. No se envía ningún mensaje si hay pendiente un reinicio del sistema. Un paquete puede usar la [**propiedad MsiSystemRebootPending**](msisystemrebootpending.md) para comprobar si hay un reinicio del sistema pendiente.

El instalador ejecuta la acción WriteEnvironmentStrings solo durante la instalación o reinstalación de un componente y ejecuta la acción [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) solo durante la eliminación de un componente.

Los valores se escriben o quitan en función de la selección de acciones y modificadores principales. Estos se describen en la siguiente sección Mensajes actionData. Tenga en cuenta que, dependiendo de la acción especificada, WriteEnvironmentStrings puede quitar variables y RemoveEnvironmentStrings puede agregarlas en función de la creación de la tabla [Environment](environment-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate](installvalidate-action.md) debe ejecutarse antes de la acción RemoveEnvironmentStrings. Dado que la acción WriteEnvironmentStrings y la acción RemoveEnvironmentStrings nunca se aplican durante una instalación o eliminación de un componente, su secuencia relativa no está restringida.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nombre de la variable de entorno que se modificará.                                                                                                                                                                                 |
| \[2\] | Valor de la variable de entorno.                                                                                                                                                                                             |
| \[3\] | Se trata de un campo de marcas de bits que especifica la acción que se va a realizar. Incluya solo un bit para una acción principal. Puede haber más de un bit modificador incluido en este campo. Consulte las siguientes descripciones de marcas de bits. |



 



| Valor de bit | Descripción de las acciones principales                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Establecer. Establece el valor de la variable de entorno en todos los casos.<br/> Si este bit se combina con un bit modificador Append o Prefix, la acción agrega el valor a cualquier valor existente de la variable.<br/> |
| 0x2       | Establecer. Establece el valor si la variable no está presente.<br/> Si este bit se combina con un bit modificador Append o Prefix, la acción agrega el valor a cualquier valor existente de la variable.<br/>                |
| 0x4       | Eliminar. Quita el valor de la variable .<br/> Si este bit se combina con un bit modificador Append o Prefix, el valor se quita de la cadena existente, si el valor existe.<br/>               |



 



| Valor de bit  | Descripción del modificador                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Si se establece este bit, las acciones se aplican a las variables de entorno de la máquina.<br/> Si no se establece este bit, las acciones se aplican a las variables de entorno del usuario.<br/> |
| 0x40000000 | Anexar. Este bit es opcional. No establezca los modificadores Append y Prefix.<br/>                                                                                            |
| 0x80000000 | Prefijo. Este bit es opcional. No establezca los modificadores Append y Prefix.<br/>                                                                                            |



 

 

 
