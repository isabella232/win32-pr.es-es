---
description: El tipo de diálogo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla Dialog proporcionada por el usuario.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158578"
---
# <a name="dialog-type"></a>Tipo de diálogo

El tipo de diálogo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la tabla [Dialog proporcionada](dialog-table.md) por el usuario.

La herramienta de combinación debe sustituir un identificador Windows [instalador válido](identifier.md) para los elementos de este tipo. Mergemod.dll no aplica esta restricción y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla Dialog.

Null es un valor válido para este tipo a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo Dialog se puede usar con los siguientes tipos de ContextData.

**DialogNext ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla de diálogos. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Dialog" en la columna Tipo y escribir "DialogNext" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla de diálogos. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Dialog" en la columna Tipo y escribir "DialogPrev" en la columna ContextData de la tabla ModuleConfiguration.

 

 



