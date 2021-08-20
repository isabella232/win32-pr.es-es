---
description: La acción RemoveEnvironmentStrings modifica los valores de las variables de entorno.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Acción RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df726dfcc6a3a5d1b2d0f2de1ab69e36f568fe4ca0c14ba6daf61d692a83beae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990776"
---
# <a name="removeenvironmentstrings-action"></a>Acción RemoveEnvironmentStrings

La acción RemoveEnvironmentStrings modifica los valores de las variables de entorno.

Tenga en cuenta que las variables de entorno no cambian para la instalación en curso cuando se ejecutan la acción [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o RemoveEnvironmentStrings. En Windows 2000, esta información se almacena en el Registro y se envía un mensaje para notificar al sistema los cambios cuando se completa la instalación. Un nuevo proceso u otro proceso que comprueba estos mensajes usará las nuevas variables de entorno.

El instalador ejecuta la [acción WriteEnvironmentStrings](writeenvironmentstrings-action.md) solo durante la instalación o reinstalación de un componente y ejecuta la acción RemoveEnvironmentStrings solo durante la eliminación de un componente.

Los valores se escriben o quitan en función de la selección de acciones y modificadores principales. Estos se describen en la siguiente sección Mensajes actionData. Tenga en cuenta que, en función de la acción especificada, WriteEnvironmentStrings puede quitar variables y RemoveEnvironmentStrings puede agregarlas en función de la creación de la tabla [Environment](environment-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallValidate](installvalidate-action.md) debe ejecutarse antes de la acción RemoveEnvironmentStrings. Dado que la acción WriteEnvironmentStrings y la acción RemoveEnvironmentStrings nunca se aplican durante la instalación o eliminación de un componente, su secuencia relativa no está restringida.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nombre de la variable de entorno que se modificará.                                                                                                                                                                               |
| \[2\] | Valor de la variable de entorno.                                                                                                                                                                                           |
| \[3\] | Se trata de un campo de marcas de bits que especifican la acción que se va a realizar. Incluya solo un bit para una acción principal. Puede haber más de un bit modificador incluido en este campo. Consulte las siguientes descripciones de marcas de bits. |



 



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



 

 

 




