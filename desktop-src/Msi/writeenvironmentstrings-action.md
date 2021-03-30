---
description: La acción WriteEnvironmentStrings modifica los valores de las variables de entorno.
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: Acción WriteEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082884"
---
# <a name="writeenvironmentstrings-action"></a>Acción WriteEnvironmentStrings

La acción WriteEnvironmentStrings modifica los valores de las variables de entorno.

Las variables de entorno no cambian para la instalación en curso cuando se ejecuta la acción WriteEnvironmentStrings o [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) . En Windows 2000, Windows Server 2003, Windows XP y Windows Vista, esta información se almacena en el registro y se envía un mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) para notificar al sistema los cambios cuando se completa la instalación. Otro proceso puede recibir notificaciones de los cambios mediante el control de estos mensajes. No se envía ningún mensaje si está pendiente un reinicio del sistema. Un paquete puede usar la propiedad [**MsiSystemRebootPending**](msisystemrebootpending.md) para comprobar si hay un reinicio del sistema pendiente.

El instalador ejecuta la acción WriteEnvironmentStrings solo durante la instalación o reinstalación de un componente, y ejecuta la [acción RemoveEnvironmentStrings](removeenvironmentstrings-action.md) solo durante la eliminación de un componente.

Los valores se escriben o se quitan en función de la selección de las acciones y modificadores principales. Se describen en la siguiente sección de mensajes de ActionData. Tenga en cuenta que, en función de la acción especificada, WriteEnvironmentStrings puede quitar variables y RemoveEnvironmentStrings puede agregarlas en función de la creación de la [tabla de entorno](environment-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate](installvalidate-action.md) se debe ejecutar antes de la acción RemoveEnvironmentStrings. Dado que la acción WriteEnvironmentStrings y la acción RemoveEnvironmentStrings nunca se aplican durante la instalación o desinstalación de un componente, su secuencia relativa no está restringida.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nombre de la variable de entorno que se va a modificar.                                                                                                                                                                                 |
| \[2\] | Valor de la variable de entorno.                                                                                                                                                                                             |
| \[3\] | Se trata de un campo de marcas de bits que especifica la acción que se va a realizar. Incluya un solo bit para una acción principal. Puede haber más de un bit modificador incluido en este campo. Vea las siguientes descripciones de marcas de bits. |



 



| Valor de bit | Descripción de las acciones principales                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Establecer. Establece el valor de la variable de entorno en todos los casos.<br/> Si este bit se combina con un bit de modificador Append o PREFIX, la acción agrega el valor a cualquier valor existente de la variable.<br/> |
| 0x2       | Establecer. Establece el valor si la variable está ausente.<br/> Si este bit se combina con un bit de modificador Append o PREFIX, la acción agrega el valor a cualquier valor existente de la variable.<br/>                |
| 0x4       | Eliminar. Quita el valor de la variable.<br/> Si este bit se combina con un bit de modificador Append o PREFIX, el valor se quita de la cadena existente, si el valor existe.<br/>               |



 



| Valor de bit  | Descripción del modificador                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Si se establece este bit, las acciones se aplican a las variables de entorno del equipo.<br/> Si no se establece este bit, las acciones se aplican a las variables de entorno del usuario.<br/> |
| 0x40000000 | Anexar. Este bit es opcional. No establezca los modificadores Append y prefix.<br/>                                                                                            |
| 0x80000000 | Ceder. Este bit es opcional. No establezca los modificadores Append y prefix.<br/>                                                                                            |



 

 

 
