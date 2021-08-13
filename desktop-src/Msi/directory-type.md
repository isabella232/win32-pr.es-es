---
description: El tipo de directorio de tipo semántico es uno de los tipos de formato de clave, que consta de una clave externa en la tabla Directory proporcionada por el usuario.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ea91ceb9baaeb2c97883cace0266a146d80634ec07f5e25f0b01ac057c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251805"
---
# <a name="directory-type"></a>Tipo de directorio

El tipo de directorio [de tipo semántico](semantic-types.md) es uno de los tipos de formato de clave [,](key-format-types.md)que consta de una clave externa en la tabla [Directory](directory-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un identificador Windows [instalador válido](identifier.md) para los elementos de este tipo. Mergemod.dll no aplica esta restricción y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla Directory.

Un elemento configurable del tipo Directory solo debe modificar el directorio de destino de la instalación y no modificar la imagen de origen. Por lo tanto, un elemento configurable de este tipo solo debe modificar las claves externas de la tabla Directory y no modificar directamente la tabla Directory.

Dado que la columna Directory de la tabla Component no acepta valores NULL, null es un valor no válido para un elemento configurable de este tipo incluso si \_ msmConfigItemNonNullable no está establecido en la columna Atributos. [](component-table.md)

El tipo Directory se puede usar con dos tipos de ContextData.

**IsolationDirectory ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los archivos del módulo. La herramienta de combinación sustituye el identificador del directorio en las plantillas de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna Nombre, escribir "1" en la columna Formato, escribir "Directorio" en la columna Tipo y escribir "IsolationDirectory" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los accesos directos del módulo. La herramienta de combinación sustituye el identificador del acceso directo por las plantillas de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna Nombre, escribir "1" en la columna Formato, escribir "Directorio" en la columna Tipo y escribir "ShortcutLocation" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

 

 



