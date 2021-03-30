---
description: El tipo de directorio de tipo semántico es uno de los tipos de formato de clave, que consta de una clave externa en la tabla de directorios proporcionada por el usuario.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910954"
---
# <a name="directory-type"></a>Tipo de directorio

El tipo de directorio de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md), que consta de una clave externa en la tabla de [directorios](directory-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo. Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla del directorio.

Un elemento configurable del tipo de directorio solo debe modificar el directorio de destino de la instalación y no modificar la imagen de origen. Por lo tanto, un elemento configurable de este tipo solo debe modificar las claves externas en la tabla del directorio y no modificar directamente la tabla de directorios.

Dado que la \_ columna de directorio de la [tabla de componentes](component-table.md) no acepta valores NULL, NULL es un valor no válido para un elemento configurable de este tipo aunque no se haya establecido msmConfigItemNonNullable en la columna Attributes.

El tipo de directorio se puede usar con dos tipos de ContextData.

**IsolationDirectory ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los archivos del módulo. La herramienta de combinación sustituye el identificador del directorio en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna nombre, escribir "1" en la columna formato, escribir "directorio" en la columna tipo y escribir "IsolationDirectory" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione un directorio de destino para los accesos directos en el módulo. La herramienta de combinación sustituye el identificador del acceso directo en las plantillas de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del directorio en la columna nombre, escribir "1" en la columna formato, escribir "directorio" en la columna tipo y escribir "ShortcutLocation" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

 

 



