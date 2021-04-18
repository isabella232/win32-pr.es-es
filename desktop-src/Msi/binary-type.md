---
description: El tipo binario de tipo semántico es uno de los tipos de formato de clave. Este tipo se compone de una clave en la tabla binaria proporcionada por el usuario.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo binario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545171"
---
# <a name="binary-type"></a>Tipo binario

El tipo binario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo se compone de una clave en la [tabla binaria](binary-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo. Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla binaria.

NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo binario se puede utilizar con los siguientes tipos de ContextData.

**Mapa de bits ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la tabla binaria que contiene una imagen de mapa de bits. Mergmod.dll no garantiza ningún tamaño o tipo de mapa de bits específico y la herramienta de combinación debe asegurarse de que los datos son una imagen válida. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "binario" en la columna tipo y escribir "bitmap" en la columna ContextData de la tabla ModuleConfiguration.

**Icono ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la tabla binaria que contiene una imagen de icono. Mergmod.dll no garantiza ningún tamaño o tipo de icono específico y la herramienta de combinación debe asegurarse de que los datos son una imagen válida. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "binario" en la columna tipo y escribir "Icon" en la columna ContextData de la tabla ModuleConfiguration. Este tipo no es adecuado para su uso en una tabla de anuncios.

**ContextData EXE**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la tabla binaria que contiene una imagen ejecutable de 32 bits. Mergmod.dll no valida que los datos sean válidos y la herramienta de combinación debe asegurarse de que los datos son un archivo PE válido. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escribir "1" en la columna formato, escribir "binario" en la columna tipo y escribir "EXE" en la columna ContextData de la tabla ModuleConfiguration.

**EXE64 ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la tabla binaria que contiene una imagen ejecutable de 32 bits o 64 bits. Mergmod.dll no valida que los datos sean válidos y la herramienta de combinación debe asegurarse de que los datos son un archivo PE válido. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "binario" en la columna tipo y escriba "EXE64" en la columna ContextData de la tabla ModuleConfiguration.

 

 



