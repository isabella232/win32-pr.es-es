---
description: El tipo de icono de tipo semántico es uno de los tipos de formato de clave. Este tipo se compone de una clave en la tabla de iconos proporcionada por el usuario.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652463"
---
# <a name="icon-type"></a>Tipo de icono

El tipo de icono de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo se compone de una clave en la [tabla de iconos](icon-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo. Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla de iconos.

NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo binario se puede utilizar con los siguientes tipos de ContextData.

**ShortcutIcon ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la [tabla de iconos](icon-table.md) que contenga una imagen adecuada para su uso como icono de acceso directo. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "Icon" en la columna Type y escriba "ShorcutIcon" en la columna ContextData de la tabla ModuleConfiguration. Este tipo no es adecuado para su uso en una tabla de interfaz de usuario. Para modificar una clave a la tabla de iconos en estas tablas, vea el icono ContextData en [tipo binario](binary-type.md).

 

 



