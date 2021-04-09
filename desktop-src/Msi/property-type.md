---
description: El tipo de propiedad de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla de propiedades proporcionada por el usuario.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082626"
---
# <a name="property-type"></a>Tipo de propiedad

El tipo de propiedad de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la [tabla de propiedades](property-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo. Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla de propiedades. Las claves principales de la tabla de propiedades son los nombres de propiedad.

NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo de propiedad se puede utilizar con los siguientes tipos de ContextData.

**ContextData null**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un nombre de propiedad a una tabla de base de datos en el módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "propiedad" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

**ContextData público**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione el nombre de una [propiedad pública](public-properties.md) a una tabla de base de datos en el módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "propiedad" en la columna tipo y escribir "público" en la columna ContextData de la tabla ModuleConfiguration.

**ContextData privado**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione el nombre de una [propiedad privada](private-properties.md) en una tabla de base de datos del módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "propiedad" en la columna tipo y escribir "privado" en la columna ContextData de la tabla ModuleConfiguration.

 

 



