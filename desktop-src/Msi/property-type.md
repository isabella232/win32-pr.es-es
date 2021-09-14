---
description: El tipo de propiedad de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla Property proporcionada por el usuario.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069740"
---
# <a name="property-type"></a>Tipo de propiedad

El tipo de propiedad de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la [tabla Property proporcionada](property-table.md) por el usuario.

La herramienta de combinación debe sustituir un identificador Windows [instalador válido](identifier.md) para los elementos de este tipo. Mergemod.dll no aplica esta restricción y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla Property. Las claves principales de la tabla Property son los nombres de propiedad.

Null es un valor válido para este tipo a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo Property puede usarse con los siguientes tipos de ContextData.

**Null ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un nombre de propiedad a una tabla de base de datos en el módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Propiedad" en la columna Tipo y dejar en blanco la columna ContextData de la tabla [ModuleConfiguration](moduleconfiguration-table.md).

**Public ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione el nombre de una propiedad [pública](public-properties.md) a una tabla de base de datos del módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Propiedad" en la columna Tipo y escribir "Público" en la columna ContextData de la tabla ModuleConfiguration.

**Private ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir al usuario proporcionar el nombre de una propiedad [privada](private-properties.md) a una tabla de base de datos del módulo. La herramienta de combinación sustituye el identificador de la propiedad en las plantillas de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Propiedad" en la columna Tipo y escribir "Privado" en la columna ContextData de la tabla ModuleConfiguration.

 

 



