---
description: El tipo binario de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave en la tabla Binaria proporcionada por el usuario.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Tipo binario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158985"
---
# <a name="binary-type"></a>Tipo binario

El tipo binario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave en la [tabla Binaria proporcionada](binary-table.md) por el usuario.

La herramienta de combinación debe sustituir un identificador Windows [instalador válido](identifier.md) para los elementos de este tipo. Mergemod.dll no aplica esta restricción y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla Binaria.

Null es un valor válido para este tipo a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo Binary se puede usar con los siguientes tipos de ContextData.

**ContextData de mapa de bits**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa a una fila de la tabla binaria que contiene una imagen de mapa de bits. Mergmod.dll no garantiza ningún tamaño o tipo específico de mapa de bits y la herramienta de combinación debe asegurarse de que los datos son una imagen válida. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Binario" en la columna Tipo y escribir "Bitmap" en la columna ContextData de la tabla ModuleConfiguration.

**Icono ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir al usuario proporcionar una clave externa a una fila de la tabla binaria que contiene una imagen de icono. Mergmod.dll no garantiza ningún tamaño o tipo específico de icono y la herramienta de combinación debe asegurarse de que los datos son una imagen válida. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Binario" en la columna Tipo y escribir "Icono" en la columna ContextData de la tabla ModuleConfiguration. Este tipo no es adecuado para su uso en una tabla de anuncios.

**EXE ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir al usuario proporcionar una clave externa a una fila de la tabla binaria que contiene una imagen ejecutable de 32 bits. Mergmod.dll no valida que los datos son válidos y la herramienta de combinación debe asegurarse de que los datos son un archivo PE válido. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Binario" en la columna Tipo y escribir "EXE" en la columna ContextData de la tabla ModuleConfiguration.

**EXE64 ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir al usuario proporcionar una clave externa a una fila de la tabla binaria que contiene una imagen ejecutable de 32 o 64 bits. Mergmod.dll no valida que los datos son válidos y la herramienta de combinación debe asegurarse de que los datos son un archivo PE válido. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Binario" en la columna Tipo y escribir "EXE64" en la columna ContextData de la tabla ModuleConfiguration.

 

 



